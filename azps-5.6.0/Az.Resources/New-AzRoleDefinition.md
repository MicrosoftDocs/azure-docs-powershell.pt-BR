---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888193"
---
# <span data-ttu-id="0c96f-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0c96f-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="0c96f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c96f-102">SYNOPSIS</span></span>
<span data-ttu-id="0c96f-103">Cria uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="0c96f-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="0c96f-104">Forneça um arquivo de definição de função JSON ou um objeto PSRoleDefinition como entrada.</span><span class="sxs-lookup"><span data-stu-id="0c96f-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="0c96f-105">Primeiro, use o comando Get-AzRoleDefinition para gerar um objeto de definição de função de linha de base.</span><span class="sxs-lookup"><span data-stu-id="0c96f-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="0c96f-106">Em seguida, modifique suas propriedades conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0c96f-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="0c96f-107">Por fim, use este comando para criar uma função personalizada usando a definição de função.</span><span class="sxs-lookup"><span data-stu-id="0c96f-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="0c96f-108">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c96f-108">SYNTAX</span></span>

### <span data-ttu-id="0c96f-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c96f-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c96f-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c96f-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c96f-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c96f-111">DESCRIPTION</span></span>
<span data-ttu-id="0c96f-112">O New-AzRoleDefinition cmdlet cria uma função personalizada no Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="0c96f-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="0c96f-113">Forneça uma definição de função como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="0c96f-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="0c96f-114">A definição da função de entrada DEVE conter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="0c96f-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="0c96f-115">DisplayName: o nome da função personalizada</span><span class="sxs-lookup"><span data-stu-id="0c96f-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="0c96f-116">Descrição: uma breve descrição da função que resume o acesso que a função concede.</span><span class="sxs-lookup"><span data-stu-id="0c96f-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="0c96f-117">Ações: o conjunto de operações às quais a função personalizada concede acesso.</span><span class="sxs-lookup"><span data-stu-id="0c96f-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="0c96f-118">Use Get-AzProviderOperation para obter a operação para provedores de recursos do Azure que podem ser protegidos usando o Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="0c96f-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="0c96f-119">A seguir estão algumas cadeias de caracteres de operação válidas:</span><span class="sxs-lookup"><span data-stu-id="0c96f-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="0c96f-120">"\*/leitura" concede acesso a operações de leitura de todos os provedores de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c96f-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="0c96f-121">"Microsoft.Network/\*/read" concede acesso a operações de leitura para todos os tipos de recursos no provedor de recursos Microsoft.Network do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c96f-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="0c96f-122">"Microsoft.Compute/virtualMachines/\*" concede acesso a todas as operações de máquinas virtuais e seus tipos de recursos filho.</span><span class="sxs-lookup"><span data-stu-id="0c96f-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="0c96f-123">AssignableScopes: o conjunto de escopos (assinaturas do Azure ou grupos de recursos) nos quais a função personalizada estará disponível para atribuição.</span><span class="sxs-lookup"><span data-stu-id="0c96f-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="0c96f-124">Usando AssignableScopes, você pode disponibilizar a função personalizada para atribuição apenas nas assinaturas ou grupos de recursos que precisam dela e não atrapalhar a experiência do usuário para o restante das assinaturas ou grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c96f-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="0c96f-125">A seguir estão alguns escopos atribuíveis válidos:</span><span class="sxs-lookup"><span data-stu-id="0c96f-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="0c96f-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": disponibiliza a função para atribuição em duas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="0c96f-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="0c96f-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": disponibiliza a função para atribuição em uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="0c96f-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="0c96f-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": disponibiliza a função para atribuição somente no grupo de recursos rede.</span><span class="sxs-lookup"><span data-stu-id="0c96f-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="0c96f-129">A definição da função de entrada PODE conter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="0c96f-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="0c96f-130">NotActions: o conjunto de operações que deve ser excluído das Ações para determinar as ações efetivas para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="0c96f-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="0c96f-131">Se houver uma operação específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotActions para exclui-la, em vez de especificar todas as operações que não a operação específica em Actions.</span><span class="sxs-lookup"><span data-stu-id="0c96f-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="0c96f-132">DataActions: o conjunto de operações de dados às quais a função personalizada concede acesso.</span><span class="sxs-lookup"><span data-stu-id="0c96f-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="0c96f-133">NotDataActions: o conjunto de operações que deve ser excluído dos DataActions para determinar as ações de dados efetivas para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="0c96f-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="0c96f-134">Se houver uma operação de dados específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar NotDataActions para exclui-la, em vez de especificar todas as operações que não a operação específica em Actions.</span><span class="sxs-lookup"><span data-stu-id="0c96f-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="0c96f-135">OBSERVAÇÃO: Se um usuário receber uma função que especifique uma operação em NotActions e também atribuída outra função concederá acesso à mesma operação - o usuário poderá executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="0c96f-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="0c96f-136">NotActions não é uma regra de negação - é simplesmente uma maneira conveniente de criar um conjunto de operações permitidas quando operações específicas precisam ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="0c96f-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="0c96f-137">A seguir está uma definição de função json de exemplo que pode ser fornecida como entrada { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="0c96f-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="0c96f-138">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c96f-138">EXAMPLES</span></span>

### <span data-ttu-id="0c96f-139">Exemplo 1: Criar usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="0c96f-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="0c96f-140">Exemplo 2: Criar usando o arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="0c96f-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="0c96f-141">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c96f-141">PARAMETERS</span></span>

### <span data-ttu-id="0c96f-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c96f-142">-DefaultProfile</span></span>
<span data-ttu-id="0c96f-143">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0c96f-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c96f-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0c96f-144">-InputFile</span></span>
<span data-ttu-id="0c96f-145">Nome do arquivo que contém uma única definição de função json.</span><span class="sxs-lookup"><span data-stu-id="0c96f-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c96f-146">-Role</span><span class="sxs-lookup"><span data-stu-id="0c96f-146">-Role</span></span>
<span data-ttu-id="0c96f-147">Objeto de definição de função.</span><span class="sxs-lookup"><span data-stu-id="0c96f-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c96f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c96f-148">CommonParameters</span></span>
<span data-ttu-id="0c96f-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c96f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c96f-150">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c96f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c96f-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c96f-151">INPUTS</span></span>

### <span data-ttu-id="0c96f-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0c96f-152">None</span></span>

## <span data-ttu-id="0c96f-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c96f-153">OUTPUTS</span></span>

### <span data-ttu-id="0c96f-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0c96f-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="0c96f-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c96f-155">NOTES</span></span>
<span data-ttu-id="0c96f-156">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="0c96f-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0c96f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c96f-157">RELATED LINKS</span></span>

[<span data-ttu-id="0c96f-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="0c96f-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="0c96f-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0c96f-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="0c96f-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0c96f-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="0c96f-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="0c96f-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

