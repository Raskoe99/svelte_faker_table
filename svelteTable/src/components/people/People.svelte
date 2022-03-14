<script>
    import { faker } from '@faker-js/faker'

    let firstName = faker.name.firstName(0)
    let lastName = faker.name.lastName()
    let fullName = firstName + " " + lastName
    let email = firstName.charAt(0).toLowerCase() + "." + lastName.toLowerCase() + "@stud.kea.dk"
    let phonenumber = faker.helpers.createCard().phone
    let avatar = faker.internet.avatar()
</script>

<tr>
    <td>{fullName}</td>
    <td>{email}</td>
    <td>{phonenumber}]</td>
    <td class="picture"><img src="{avatar}" alt="avatar"></td>
</tr>

<style>
    td {
        border: 2px solid black;
        padding: 0px;
    }
    .picture {
        padding: auto;
    }
</style>