export default async function Page() {
  const data = await sql`SELECT * from USERS`;

  return (
    <>
      <h1>Users</h1>
      <ul>
        {data.map(user => (
          <li key={user.id}>
            {user.name}
          </li>
        )}
      </ul>
    </>
  );
}
