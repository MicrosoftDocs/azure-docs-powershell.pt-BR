---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 413f0e22139abe26a2be34a607587042739df1d5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785192"
---
# <span data-ttu-id="3d714-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d714-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="3d714-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3d714-102">SYNOPSIS</span></span>
<span data-ttu-id="3d714-103">Concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar operações com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d714-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d714-104">SYNTAX</span></span>

### <span data-ttu-id="3d714-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d714-105">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d714-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d714-106">ByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d714-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="3d714-107">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d714-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d714-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d714-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="3d714-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d714-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3d714-110">DESCRIPTION</span></span>
<span data-ttu-id="3d714-111">O cmdlet **set-AzureRmKeyVaultAccessPolicy** concede ou modifica permissões existentes para um usuário, aplicativo ou grupo de segurança para executar as operações especificadas com um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-111">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="3d714-112">Ele não modifica as permissões que outros usuários, aplicativos ou grupos de segurança têm no cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="3d714-113">Se você estiver definindo permissões para um grupo de segurança, essa operação afetará apenas os usuários desse grupo de segurança.</span><span class="sxs-lookup"><span data-stu-id="3d714-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="3d714-114">Todos os diretórios a seguir devem ser do mesmo diretório do Azure:</span><span class="sxs-lookup"><span data-stu-id="3d714-114">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="3d714-115">O diretório padrão da assinatura do Azure em que o cofre de chaves reside.</span><span class="sxs-lookup"><span data-stu-id="3d714-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="3d714-116">O diretório do Azure que contém o usuário ou o grupo de aplicativos aos quais você está concedendo permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="3d714-117">Exemplos de cenários quando essas condições não são atendidas e esse cmdlet não funcionará:</span><span class="sxs-lookup"><span data-stu-id="3d714-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="3d714-118">Autorizar um usuário de outra organização a gerenciar seu cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="3d714-119">Cada organização tem seu próprio diretório.</span><span class="sxs-lookup"><span data-stu-id="3d714-119">Each organization has its own directory.</span></span> 
- <span data-ttu-id="3d714-120">Sua conta do Azure tem vários diretórios.</span><span class="sxs-lookup"><span data-stu-id="3d714-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="3d714-121">Se você registrar um aplicativo em um diretório diferente do diretório padrão, não poderá autorizar esse aplicativo a usar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="3d714-122">O aplicativo deve estar no diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="3d714-122">The application must be in the default directory.</span></span>

<span data-ttu-id="3d714-123">Observe que, embora a especificação do grupo de recursos seja opcional para esse cmdlet, você deve fazê-lo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3d714-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="3d714-124">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d714-124">EXAMPLES</span></span>

### <span data-ttu-id="3d714-125">Exemplo 1: conceder permissões a um usuário para um cofre de chaves e modificar as permissões</span><span class="sxs-lookup"><span data-stu-id="3d714-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets 'set,delete'
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="3d714-126">O primeiro comando concede permissões para um usuário em seu Active Directory do Azure, PattiFuller@contoso.com para executar operações em chaves e segredos com um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3d714-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="3d714-127">O segundo comando modifica as permissões que foram concedidas ao PattiFuller@contoso.com primeiro comando, a fim de permitir a obtenção de segredos, além de definir e excluir essas permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="3d714-128">As permissões para operações de chave permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="3d714-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="3d714-129">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d714-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="3d714-130">O último comando modifica as permissões existentes para PattiFuller@contoso.com remover todas as permissões para operações de chave.</span><span class="sxs-lookup"><span data-stu-id="3d714-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="3d714-131">As permissões para operações secretas permanecem inalteradas após esse comando.</span><span class="sxs-lookup"><span data-stu-id="3d714-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="3d714-132">O parâmetro *PassThru* resulta no objeto atualizado sendo retornado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d714-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="3d714-133">Exemplo 2: conceder permissões para uma entidade de serviço de aplicativo para ler e gravar segredos</span><span class="sxs-lookup"><span data-stu-id="3d714-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3d714-134">Esse comando concede permissões para um aplicativo para um cofre de chaves chamado Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="3d714-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="3d714-135">O parâmetro *servicePrincipalName* especifica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d714-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="3d714-136">O aplicativo deve ser registrado no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d714-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="3d714-137">*O valor do parâmetro servicePrincipalName* deve ser o nome principal do aplicativo ou o GUID da ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d714-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="3d714-138">Este exemplo especifica o nome principal do serviço http://payroll.contoso.com , e o comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="3d714-138">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="3d714-139">Exemplo 3: conceder permissões para um aplicativo usando sua ID de objeto</span><span class="sxs-lookup"><span data-stu-id="3d714-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="3d714-140">Esse comando concede as permissões do aplicativo para ler e gravar segredos.</span><span class="sxs-lookup"><span data-stu-id="3d714-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="3d714-141">Este exemplo especifica o aplicativo que usa a ID de objeto da entidade de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3d714-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="3d714-142">Exemplo 4: conceder permissões para um nome de usuário principal</span><span class="sxs-lookup"><span data-stu-id="3d714-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="3d714-143">Esse comando concede a obter, listar e definir permissões para o nome principal do usuário especificado para acessar os segredos.</span><span class="sxs-lookup"><span data-stu-id="3d714-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="3d714-144">Exemplo 5: habilitar os segredos para serem recuperados de um cofre de chaves pelo provedor de recursos Microsoft. Compute</span><span class="sxs-lookup"><span data-stu-id="3d714-144">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="3d714-145">Esse comando concede as permissões para que os segredos sejam recuperados do cofre da chave Contoso03Vault pelo provedor de recursos Microsoft. COMPUTE.</span><span class="sxs-lookup"><span data-stu-id="3d714-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="3d714-146">Exemplo 6: conceder permissões a um grupo de segurança</span><span class="sxs-lookup"><span data-stu-id="3d714-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="3d714-147">O primeiro comando usa o cmdlet Get-AzureRmADGroup para obter todos os grupos do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d714-147">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="3d714-148">Na saída, você verá 3 grupos retornados, chamados **grupo1** , **group2** e **Group3**.</span><span class="sxs-lookup"><span data-stu-id="3d714-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="3d714-149">Vários grupos podem ter o mesmo nome, mas sempre têm um ObjectId exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3d714-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="3d714-150">Quando mais de um grupo com o mesmo nome for retornado, use o ObjectId na saída para identificar o que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="3d714-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="3d714-151">Em seguida, você usa a saída desse comando com Set-AzureRmKeyVaultAccessPolicy para conceder permissões a group2 para o seu cofre de chaves, chamado **myownvault**.</span><span class="sxs-lookup"><span data-stu-id="3d714-151">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="3d714-152">Este exemplo enumera os grupos chamados "group2" embutidos na mesma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3d714-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="3d714-153">Pode haver vários grupos na lista retornada com o nome "group2".</span><span class="sxs-lookup"><span data-stu-id="3d714-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="3d714-154">Este exemplo escolhe o primeiro, indicado pelo índice \[ 0 \] na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="3d714-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="3d714-155">Exemplo 7: conceder ao Azure acesso à proteção de informações à chave locatário gerenciada pelo cliente (BYOK)</span><span class="sxs-lookup"><span data-stu-id="3d714-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="3d714-156">Esse comando autoriza a proteção de informações do Azure a usar uma chave gerenciada pelo cliente (a traga sua própria chave ou o cenário "BYOK") como a chave locatário do Azure Information Protection.</span><span class="sxs-lookup"><span data-stu-id="3d714-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="3d714-157">Ao executar esse comando, especifique seu próprio nome do cofre de chaves, mas você deve especificar o parâmetro *servicePrincipalName* com o GUID **00000012-0000-0000-C000-000000000000** e especificar as permissões no exemplo.</span><span class="sxs-lookup"><span data-stu-id="3d714-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="3d714-158">OS</span><span class="sxs-lookup"><span data-stu-id="3d714-158">PARAMETERS</span></span>

### <span data-ttu-id="3d714-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3d714-159">-ApplicationId</span></span>
<span data-ttu-id="3d714-160">Para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3d714-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="3d714-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="3d714-162">Permite que você especifique uma ID de objeto sem validar que o objeto existe no Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3d714-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="3d714-163">Use esse parâmetro somente se você quiser conceder acesso ao seu cofre de chaves a uma ID de objeto que se refere a um grupo de segurança delegado de outro locatário do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d714-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d714-164">-DefaultProfile</span></span>
<span data-ttu-id="3d714-165">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3d714-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3d714-166">-EmailAddress</span></span>
<span data-ttu-id="3d714-167">Especifica o endereço de email do usuário para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="3d714-168">Esse endereço de email deve existir no diretório associado à assinatura atual e ser exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3d714-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="3d714-169">-EnabledForDeployment</span></span>
<span data-ttu-id="3d714-170">Habilita o provedor de recursos Microsoft. Compute a recuperar segredos deste cofre de chaves quando esse cofre de chaves é referenciado na criação de recursos, por exemplo, ao criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3d714-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="3d714-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="3d714-172">Habilita o serviço de criptografia de disco do Azure a obter segredos e a desencapsulação de chaves deste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="3d714-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="3d714-174">Permite que o Azure Resource Manager obtenha os segredos deste cofre de chaves quando esse cofre de chaves é referenciado em uma implantação de modelo.</span><span class="sxs-lookup"><span data-stu-id="3d714-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3d714-175">-ObjectId</span></span>
<span data-ttu-id="3d714-176">Especifica a ID de objeto da entidade de usuário ou serviço do Azure Active Directory para a qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d714-177">-PassThru</span></span>
<span data-ttu-id="3d714-178">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3d714-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="3d714-179">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3d714-179">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="3d714-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="3d714-181">Especifica uma matriz de permissões de certificado a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d714-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3d714-182">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="3d714-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3d714-183">Obter</span><span class="sxs-lookup"><span data-stu-id="3d714-183">Get</span></span>
- <span data-ttu-id="3d714-184">Programação</span><span class="sxs-lookup"><span data-stu-id="3d714-184">List</span></span>
- <span data-ttu-id="3d714-185">Remover</span><span class="sxs-lookup"><span data-stu-id="3d714-185">Delete</span></span>
- <span data-ttu-id="3d714-186">Criados</span><span class="sxs-lookup"><span data-stu-id="3d714-186">Create</span></span>
- <span data-ttu-id="3d714-187">Importações</span><span class="sxs-lookup"><span data-stu-id="3d714-187">Import</span></span>
- <span data-ttu-id="3d714-188">Atualização</span><span class="sxs-lookup"><span data-stu-id="3d714-188">Update</span></span>
- <span data-ttu-id="3d714-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="3d714-189">Managecontacts</span></span>
- <span data-ttu-id="3d714-190">Emissors</span><span class="sxs-lookup"><span data-stu-id="3d714-190">Getissuers</span></span>
- <span data-ttu-id="3d714-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="3d714-191">Listissuers</span></span>
- <span data-ttu-id="3d714-192">Emissores</span><span class="sxs-lookup"><span data-stu-id="3d714-192">Setissuers</span></span>
- <span data-ttu-id="3d714-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="3d714-193">Deleteissuers</span></span>
- <span data-ttu-id="3d714-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="3d714-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-195">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="3d714-195">-PermissionsToKeys</span></span>
<span data-ttu-id="3d714-196">Especifica uma matriz de permissões de operações de chave a serem concedidas a um usuário ou serviço principal.</span><span class="sxs-lookup"><span data-stu-id="3d714-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3d714-197">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="3d714-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3d714-198">Criptografá</span><span class="sxs-lookup"><span data-stu-id="3d714-198">Decrypt</span></span>
- <span data-ttu-id="3d714-199">Com</span><span class="sxs-lookup"><span data-stu-id="3d714-199">Encrypt</span></span>
- <span data-ttu-id="3d714-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="3d714-200">UnwrapKey</span></span>
- <span data-ttu-id="3d714-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="3d714-201">WrapKey</span></span>
- <span data-ttu-id="3d714-202">Verificar</span><span class="sxs-lookup"><span data-stu-id="3d714-202">Verify</span></span>
- <span data-ttu-id="3d714-203">Designa</span><span class="sxs-lookup"><span data-stu-id="3d714-203">Sign</span></span>
- <span data-ttu-id="3d714-204">Obter</span><span class="sxs-lookup"><span data-stu-id="3d714-204">Get</span></span>
- <span data-ttu-id="3d714-205">Programação</span><span class="sxs-lookup"><span data-stu-id="3d714-205">List</span></span>
- <span data-ttu-id="3d714-206">Atualização</span><span class="sxs-lookup"><span data-stu-id="3d714-206">Update</span></span>
- <span data-ttu-id="3d714-207">Criados</span><span class="sxs-lookup"><span data-stu-id="3d714-207">Create</span></span>
- <span data-ttu-id="3d714-208">Importações</span><span class="sxs-lookup"><span data-stu-id="3d714-208">Import</span></span>
- <span data-ttu-id="3d714-209">Remover</span><span class="sxs-lookup"><span data-stu-id="3d714-209">Delete</span></span>
- <span data-ttu-id="3d714-210">Fazer</span><span class="sxs-lookup"><span data-stu-id="3d714-210">Backup</span></span>
- <span data-ttu-id="3d714-211">Restaurar</span><span class="sxs-lookup"><span data-stu-id="3d714-211">Restore</span></span>
- <span data-ttu-id="3d714-212">Gravação</span><span class="sxs-lookup"><span data-stu-id="3d714-212">Recover</span></span>
- <span data-ttu-id="3d714-213">Purga</span><span class="sxs-lookup"><span data-stu-id="3d714-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-214">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="3d714-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="3d714-215">Especifica uma matriz de permissões de operação secreta a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d714-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="3d714-216">Os valores aceitáveis para esse parâmetro:</span><span class="sxs-lookup"><span data-stu-id="3d714-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="3d714-217">Obter</span><span class="sxs-lookup"><span data-stu-id="3d714-217">Get</span></span>
- <span data-ttu-id="3d714-218">Programação</span><span class="sxs-lookup"><span data-stu-id="3d714-218">List</span></span>
- <span data-ttu-id="3d714-219">Configurar</span><span class="sxs-lookup"><span data-stu-id="3d714-219">Set</span></span>
- <span data-ttu-id="3d714-220">Remover</span><span class="sxs-lookup"><span data-stu-id="3d714-220">Delete</span></span>
- <span data-ttu-id="3d714-221">Fazer</span><span class="sxs-lookup"><span data-stu-id="3d714-221">Backup</span></span>
- <span data-ttu-id="3d714-222">Restaurar</span><span class="sxs-lookup"><span data-stu-id="3d714-222">Restore</span></span>
- <span data-ttu-id="3d714-223">Gravação</span><span class="sxs-lookup"><span data-stu-id="3d714-223">Recover</span></span>
- <span data-ttu-id="3d714-224">Purga</span><span class="sxs-lookup"><span data-stu-id="3d714-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-225">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="3d714-225">-PermissionsToStorage</span></span>
<span data-ttu-id="3d714-226">Especifica as permissões da conta de armazenamento gerenciado e da operação de definição SaS a serem concedidas a um usuário ou entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d714-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases: 
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d714-227">-ResourceGroupName</span></span>
<span data-ttu-id="3d714-228">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3d714-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-229">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="3d714-229">-ServicePrincipalName</span></span>
<span data-ttu-id="3d714-230">Especifica o nome principal do serviço do aplicativo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="3d714-231">Especifique o ID do aplicativo, também conhecido como ID do cliente, registrado para o aplicativo no diretório AzureActive.</span><span class="sxs-lookup"><span data-stu-id="3d714-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="3d714-232">O aplicativo com o nome da entidade de serviço que esse parâmetro especifica deve ser registrado no diretório do Azure que contém sua assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3d714-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="3d714-233">-UserPrincipalName</span></span>
<span data-ttu-id="3d714-234">Especifica o nome UPN do usuário a quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="3d714-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="3d714-235">Este nome de usuário principal deve existir no diretório associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3d714-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-236">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3d714-236">-VaultName</span></span>
<span data-ttu-id="3d714-237">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3d714-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="3d714-238">Esse cmdlet modifica a política de acesso para o cofre de chaves que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3d714-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-239">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3d714-239">-Confirm</span></span>
<span data-ttu-id="3d714-240">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d714-240">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d714-241">-WhatIf</span></span>
<span data-ttu-id="3d714-242">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3d714-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d714-243">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3d714-243">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d714-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d714-244">CommonParameters</span></span>
<span data-ttu-id="3d714-245">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d714-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d714-246">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d714-246">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d714-247">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3d714-247">INPUTS</span></span>

### <span data-ttu-id="3d714-248">String, GUID, String [], switch</span><span class="sxs-lookup"><span data-stu-id="3d714-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="3d714-249">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3d714-249">OUTPUTS</span></span>

### <span data-ttu-id="3d714-250">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="3d714-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="3d714-251">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3d714-251">NOTES</span></span>

## <span data-ttu-id="3d714-252">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d714-252">RELATED LINKS</span></span>

[<span data-ttu-id="3d714-253">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="3d714-253">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="3d714-254">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3d714-254">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)

