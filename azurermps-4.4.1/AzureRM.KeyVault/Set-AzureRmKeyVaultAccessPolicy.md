---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://go.microsoft.com/fwlink/?LinkId=690163
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 9ebf606a41a3a972b2d636846fbdc7834388ef29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440632"
---
# <span data-ttu-id="8d13f-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d13f-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="8d13f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d13f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d13f-103">Concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar operações com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d13f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d13f-104">SYNTAX</span></span>

### <span data-ttu-id="8d13f-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d13f-105">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d13f-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d13f-106">ByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d13f-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="8d13f-107">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d13f-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d13f-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d13f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="8d13f-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d13f-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d13f-110">DESCRIPTION</span></span>
<span data-ttu-id="8d13f-111">O cmdlet **set-AzureRmKeyVaultAccessPolicy** concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar as operações especificadas com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-111">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span>
<span data-ttu-id="8d13f-112">Ele não modifica as permissões que outros usuários, aplicativos ou grupos de segurança têm no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="8d13f-113">Se você estiver definindo permissões para um grupo de segurança, essa operação afetará apenas os usuários desse grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="8d13f-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="8d13f-114">Todos os diretórios a seguir devem ser do mesmo diretório do Azure:</span><span class="sxs-lookup"><span data-stu-id="8d13f-114">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="8d13f-115">O diretório padrão da assinatura do Azure em que o cofre de chaves reside.</span><span class="sxs-lookup"><span data-stu-id="8d13f-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="8d13f-116">O diretório do Azure que contém o usuário ou o grupo de aplicativos aos quais você está concedendo permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="8d13f-117">Exemplos de cenários quando essas condições não são atendidas e esse cmdlet não funcionará:</span><span class="sxs-lookup"><span data-stu-id="8d13f-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="8d13f-118">Autorizar um usuário de outra organização a gerenciar seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="8d13f-119">Cada organização tem seu próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="8d13f-119">Each organization has its own directory.</span></span> 
- <span data-ttu-id="8d13f-120">Sua conta do Azure tem vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="8d13f-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="8d13f-121">Se você registrar um aplicativo em um diretório diferente do diretório padrão, não poderá autorizar esse aplicativo a usar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="8d13f-122">O aplicativo deve estar no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="8d13f-122">The application must be in the default directory.</span></span>

<span data-ttu-id="8d13f-123">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8d13f-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="8d13f-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d13f-124">EXAMPLES</span></span>

### <span data-ttu-id="8d13f-125">Exemplo 1: conceder permissões a um usuário para um cofre da chave do cofre e modificar o cofre permissionskey</span><span class="sxs-lookup"><span data-stu-id="8d13f-125">Example 1: Grant permissions to a user for a key vault Key Vault and modify the permissionskey vault</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="8d13f-126">O primeiro comando concede permissões para um usuário em seu Active Directory do Azure, PattiFuller@contoso.com para executar operações em chaves e segredos com um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8d13f-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="8d13f-127">O segundo comando modifica as permissões que foram concedidas ao PattiFuller@contoso.com primeiro comando, a fim de permitir a obtenção de segredos, além de definir e excluir essas permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span>
<span data-ttu-id="8d13f-128">As permissões para operações de chave permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="8d13f-128">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="8d13f-129">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d13f-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="8d13f-130">O último comando modifica as permissões existentes para PattiFuller@contoso.com remover todas as permissões para operações de chave.</span><span class="sxs-lookup"><span data-stu-id="8d13f-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span>
<span data-ttu-id="8d13f-131">As permissões para operações secretas permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="8d13f-131">The permissions to secret operations remain unchanged after this command.</span></span>
<span data-ttu-id="8d13f-132">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d13f-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="8d13f-133">Exemplo 2: conceder permissões para uma entidade de serviço de aplicativo para ler e gravar segredos</span><span class="sxs-lookup"><span data-stu-id="8d13f-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8d13f-134">Esse comando concede permissões para um aplicativo para um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="8d13f-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="8d13f-135">O parâmetro *servicePrincipalName* especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-135">The *ServicePrincipalName* parameter specifies the application.</span></span>
<span data-ttu-id="8d13f-136">O aplicativo deve ser registrado no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d13f-136">The application must be registered in your Azure Active Directory.</span></span>
<span data-ttu-id="8d13f-137">*O valor do parâmetro servicePrincipalName* deve ser o nome principal do aplicativo ou o GUID da ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="8d13f-138">Este exemplo especifica o nome principal do serviço http://payroll.contoso.com , e o comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="8d13f-138">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="8d13f-139">Exemplo 3: conceder permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="8d13f-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="8d13f-140">Esse comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="8d13f-140">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="8d13f-141">Este exemplo especifica o aplicativo que usa a ID de objeto da entidade de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="8d13f-142">Exemplo 4: conceder permissões para um nome de usuário principal</span><span class="sxs-lookup"><span data-stu-id="8d13f-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="8d13f-143">Esse comando concede a obter, listar e definir permissões para o nome principal do usuário especificado para acessar os segredos.</span><span class="sxs-lookup"><span data-stu-id="8d13f-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="8d13f-144">Exemplo 5: habilitar os segredos para serem recuperados de um cofre de chaves pelo cofre do recurso Microsoft. Compute providerkey</span><span class="sxs-lookup"><span data-stu-id="8d13f-144">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource providerkey vault</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="8d13f-145">Esse comando concede as permissões para que os segredos sejam recuperados do cofre da chave Contoso03Vault pelo provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="8d13f-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="8d13f-146">Exemplo 6: conceder permissões a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="8d13f-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="8d13f-147">O primeiro comando usa o cmdlet Get-AzureRmADGroup para obter todos os grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d13f-147">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span>
<span data-ttu-id="8d13f-148">Na saída, você verá 3 grupos retornados, chamados **grupo1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="8d13f-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span>
<span data-ttu-id="8d13f-149">Vários grupos podem ter o mesmo nome, mas sempre têm um ObjectId exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span>
<span data-ttu-id="8d13f-150">Quando mais de um grupo com o mesmo nome for retornado, use o ObjectId na saída para identificar o que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="8d13f-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="8d13f-151">Em seguida, você usa a saída desse comando com Set-AzureRmKeyVaultAccessPolicy para conceder permissões a group2 para o seu cofre de chaves, chamado **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="8d13f-151">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span>
<span data-ttu-id="8d13f-152">Este exemplo enumera os grupos chamados "group2" embutidos na mesma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8d13f-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="8d13f-153">Pode haver vários grupos na lista retornada com o nome "group2".</span><span class="sxs-lookup"><span data-stu-id="8d13f-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="8d13f-154">Este exemplo escolhe o primeiro, indicado pelo índice \[ 0 \] na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="8d13f-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="8d13f-155">Exemplo 7: conceder ao Azure acesso à proteção de informações à chave locatário gerenciada pelo cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="8d13f-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,encrypt,unwrapkey,wrapkey,verify,sign,get
```

<span data-ttu-id="8d13f-156">Esse comando autoriza a proteção de informações do Azure a usar uma chave gerenciada pelo cliente (a traga sua própria chave ou o cenário "BYOK") como a chave locatário do Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="8d13f-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="8d13f-157">Ao executar esse comando, especifique seu próprio nome de cofre, mas você deve especificar o parâmetro *servicePrincipalName* com o GUID **00000012-0000-0000-C000-000000000000** e especificar todas as permissões no exemplo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-157">When you run this command, specify your own vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify all the permissions in the example.</span></span>

## <span data-ttu-id="8d13f-158">OS</span><span class="sxs-lookup"><span data-stu-id="8d13f-158">PARAMETERS</span></span>

### <span data-ttu-id="8d13f-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8d13f-159">-ApplicationId</span></span>
<span data-ttu-id="8d13f-160">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="8d13f-160">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="8d13f-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="8d13f-162">Permite que você especifique uma ID de objeto sem validar que o objeto existe no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8d13f-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="8d13f-163">Use esse parâmetro somente se você quiser conceder acesso ao seu cofre de chaves a uma ID de objeto que se refere a um grupo de segurança delegado de outro locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d13f-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-164">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8d13f-164">-EmailAddress</span></span>
<span data-ttu-id="8d13f-165">Especifica o endereço de email do usuário para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-165">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8d13f-166">Esse endereço de email deve existir no diretório associado à assinatura atual e ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-166">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-167">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="8d13f-167">-EnabledForDeployment</span></span>
<span data-ttu-id="8d13f-168">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8d13f-168">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-169">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="8d13f-169">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="8d13f-170">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-170">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-171">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="8d13f-171">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="8d13f-172">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="8d13f-172">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-173">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8d13f-173">-ObjectId</span></span>
<span data-ttu-id="8d13f-174">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-174">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-175">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d13f-175">-PassThru</span></span>
<span data-ttu-id="8d13f-176">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8d13f-176">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8d13f-177">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8d13f-177">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-178">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="8d13f-178">-PermissionsToCertificates</span></span>
<span data-ttu-id="8d13f-179">Especifica uma matriz de permissões de certificado a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8d13f-179">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d13f-180">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8d13f-180">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d13f-181">Obter</span><span class="sxs-lookup"><span data-stu-id="8d13f-181">Get</span></span>
- <span data-ttu-id="8d13f-182">Programação</span><span class="sxs-lookup"><span data-stu-id="8d13f-182">List</span></span>
- <span data-ttu-id="8d13f-183">Remover</span><span class="sxs-lookup"><span data-stu-id="8d13f-183">Delete</span></span>
- <span data-ttu-id="8d13f-184">Criados</span><span class="sxs-lookup"><span data-stu-id="8d13f-184">Create</span></span>
- <span data-ttu-id="8d13f-185">Importações</span><span class="sxs-lookup"><span data-stu-id="8d13f-185">Import</span></span>
- <span data-ttu-id="8d13f-186">Atualização</span><span class="sxs-lookup"><span data-stu-id="8d13f-186">Update</span></span>
- <span data-ttu-id="8d13f-187">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="8d13f-187">Managecontacts</span></span>
- <span data-ttu-id="8d13f-188">Emissors</span><span class="sxs-lookup"><span data-stu-id="8d13f-188">Getissuers</span></span>
- <span data-ttu-id="8d13f-189">Listissuers</span><span class="sxs-lookup"><span data-stu-id="8d13f-189">Listissuers</span></span>
- <span data-ttu-id="8d13f-190">Emissores</span><span class="sxs-lookup"><span data-stu-id="8d13f-190">Setissuers</span></span>
- <span data-ttu-id="8d13f-191">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="8d13f-191">Deleteissuers</span></span>
- <span data-ttu-id="8d13f-192">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="8d13f-192">Manageissuers</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-193">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="8d13f-193">-PermissionsToKeys</span></span>
<span data-ttu-id="8d13f-194">Especifica uma matriz de permissões de operações de chave a serem concedidas a um usuário ou serviço principal.</span><span class="sxs-lookup"><span data-stu-id="8d13f-194">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d13f-195">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8d13f-195">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d13f-196">Criptografá</span><span class="sxs-lookup"><span data-stu-id="8d13f-196">Decrypt</span></span>
- <span data-ttu-id="8d13f-197">Com</span><span class="sxs-lookup"><span data-stu-id="8d13f-197">Encrypt</span></span>
- <span data-ttu-id="8d13f-198">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="8d13f-198">UnwrapKey</span></span>
- <span data-ttu-id="8d13f-199">WrapKey</span><span class="sxs-lookup"><span data-stu-id="8d13f-199">WrapKey</span></span>
- <span data-ttu-id="8d13f-200">Verificar</span><span class="sxs-lookup"><span data-stu-id="8d13f-200">Verify</span></span>
- <span data-ttu-id="8d13f-201">Designa</span><span class="sxs-lookup"><span data-stu-id="8d13f-201">Sign</span></span>
- <span data-ttu-id="8d13f-202">Obter</span><span class="sxs-lookup"><span data-stu-id="8d13f-202">Get</span></span>
- <span data-ttu-id="8d13f-203">Programação</span><span class="sxs-lookup"><span data-stu-id="8d13f-203">List</span></span>
- <span data-ttu-id="8d13f-204">Atualização</span><span class="sxs-lookup"><span data-stu-id="8d13f-204">Update</span></span>
- <span data-ttu-id="8d13f-205">Criados</span><span class="sxs-lookup"><span data-stu-id="8d13f-205">Create</span></span>
- <span data-ttu-id="8d13f-206">Importações</span><span class="sxs-lookup"><span data-stu-id="8d13f-206">Import</span></span>
- <span data-ttu-id="8d13f-207">Remover</span><span class="sxs-lookup"><span data-stu-id="8d13f-207">Delete</span></span>
- <span data-ttu-id="8d13f-208">Fazer</span><span class="sxs-lookup"><span data-stu-id="8d13f-208">Backup</span></span>
- <span data-ttu-id="8d13f-209">Restaurar</span><span class="sxs-lookup"><span data-stu-id="8d13f-209">Restore</span></span>
- <span data-ttu-id="8d13f-210">Gravação</span><span class="sxs-lookup"><span data-stu-id="8d13f-210">Recover</span></span>
- <span data-ttu-id="8d13f-211">Purga</span><span class="sxs-lookup"><span data-stu-id="8d13f-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-212">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="8d13f-212">-PermissionsToSecrets</span></span>
<span data-ttu-id="8d13f-213">Especifica uma matriz de permissões de operação secreta a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8d13f-213">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="8d13f-214">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8d13f-214">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d13f-215">Obter</span><span class="sxs-lookup"><span data-stu-id="8d13f-215">Get</span></span>
- <span data-ttu-id="8d13f-216">Programação</span><span class="sxs-lookup"><span data-stu-id="8d13f-216">List</span></span>
- <span data-ttu-id="8d13f-217">Configurar</span><span class="sxs-lookup"><span data-stu-id="8d13f-217">Set</span></span>
- <span data-ttu-id="8d13f-218">Remover</span><span class="sxs-lookup"><span data-stu-id="8d13f-218">Delete</span></span>
- <span data-ttu-id="8d13f-219">Fazer</span><span class="sxs-lookup"><span data-stu-id="8d13f-219">Backup</span></span>
- <span data-ttu-id="8d13f-220">Restaurar</span><span class="sxs-lookup"><span data-stu-id="8d13f-220">Restore</span></span>
- <span data-ttu-id="8d13f-221">Gravação</span><span class="sxs-lookup"><span data-stu-id="8d13f-221">Recover</span></span>
- <span data-ttu-id="8d13f-222">Purga</span><span class="sxs-lookup"><span data-stu-id="8d13f-222">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-223">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="8d13f-223">-PermissionsToStorage</span></span>
<span data-ttu-id="8d13f-224">Especifica as permissões da conta de armazenamento gerenciado e da operação de definição SAS para conceder a um usuário ou serviço de entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="8d13f-224">Specifies managed storage account and sas definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-225">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d13f-225">-ResourceGroupName</span></span>
<span data-ttu-id="8d13f-226">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d13f-226">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-227">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="8d13f-227">-ServicePrincipalName</span></span>
<span data-ttu-id="8d13f-228">Especifica o nome principal do serviço do aplicativo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-228">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="8d13f-229">Especifique o ID do aplicativo, também conhecido como ID do cliente, registrado para o aplicativo no diretório AzureActive.</span><span class="sxs-lookup"><span data-stu-id="8d13f-229">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span>
<span data-ttu-id="8d13f-230">O aplicativo com o nome da entidade de serviço que esse parâmetro especifica deve ser registrado no diretório do Azure que contém sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8d13f-230">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-231">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8d13f-231">-UserPrincipalName</span></span>
<span data-ttu-id="8d13f-232">Especifica o nome UPN do usuário a quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="8d13f-232">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="8d13f-233">Este nome de usuário principal deve existir no diretório associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="8d13f-233">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-234">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8d13f-234">-VaultName</span></span>
<span data-ttu-id="8d13f-235">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8d13f-235">Specifies the name of a key vault.</span></span>
<span data-ttu-id="8d13f-236">Esse cmdlet modifica a política de acesso para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8d13f-236">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-237">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d13f-237">-Confirm</span></span>
<span data-ttu-id="8d13f-238">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d13f-238">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-239">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d13f-239">-WhatIf</span></span>
<span data-ttu-id="8d13f-240">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d13f-240">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d13f-241">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d13f-241">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-242">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d13f-242">-DefaultProfile</span></span>
<span data-ttu-id="8d13f-243">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d13f-243">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d13f-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d13f-244">CommonParameters</span></span>
<span data-ttu-id="8d13f-245">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d13f-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d13f-246">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d13f-246">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d13f-247">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d13f-247">INPUTS</span></span>

### <span data-ttu-id="8d13f-248">String, GUID, String [], switch</span><span class="sxs-lookup"><span data-stu-id="8d13f-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="8d13f-249">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d13f-249">OUTPUTS</span></span>

### <span data-ttu-id="8d13f-250">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="8d13f-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="8d13f-251">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d13f-251">NOTES</span></span>

## <span data-ttu-id="8d13f-252">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d13f-252">RELATED LINKS</span></span>

[<span data-ttu-id="8d13f-253">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="8d13f-253">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="8d13f-254">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8d13f-254">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

