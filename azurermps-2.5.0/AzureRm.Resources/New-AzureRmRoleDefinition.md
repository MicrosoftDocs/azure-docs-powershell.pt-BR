---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: bf3df91cc8b35ad2c61d277b12ad234a8034d207
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785847"
---
# <span data-ttu-id="b9c1e-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c1e-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="b9c1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c1e-103">Cria uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="b9c1e-104">Forneça um arquivo de definição de função JSON ou um objeto PSRoleDefinition como entrada.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="b9c1e-105">Primeiro, use o comando Get-AzureRmRoleDefinition para gerar um objeto de definição de função de linha de base.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="b9c1e-106">Em seguida, modifique suas propriedades conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="b9c1e-107">Por fim, use esse comando para criar uma função personalizada usando definição de função.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c1e-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c1e-108">SYNTAX</span></span>

### <span data-ttu-id="b9c1e-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c1e-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c1e-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c1e-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c1e-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9c1e-111">DESCRIPTION</span></span>
<span data-ttu-id="b9c1e-112">O cmdlet New-AzureRmRoleDefinition cria uma função personalizada no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="b9c1e-113">Forneça uma definição de função como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="b9c1e-114">A definição da função de entrada deve conter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="b9c1e-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="b9c1e-115">DisplayName: o nome da função personalizada</span><span class="sxs-lookup"><span data-stu-id="b9c1e-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="b9c1e-116">Descrição: uma breve descrição da função que resume o acesso concedido pela função.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="b9c1e-117">Ações: o conjunto de operações às quais a função personalizada concede acesso.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="b9c1e-118">Use Get-AzureRmProviderOperation para obter a operação dos provedores de recursos do Azure que podem ser protegidos usando o Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-118">Use Get-AzureRmProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="b9c1e-119">Veja a seguir algumas cadeias de caracteres de operação válidas:</span><span class="sxs-lookup"><span data-stu-id="b9c1e-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="b9c1e-120">"\*/Read" concede acesso a operações de leitura de todos os provedores de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="b9c1e-121">"Microsoft. Network/\*/Read" concede acesso a operações de leitura para todos os tipos de recursos do provedor de recursos da Microsoft. Network do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="b9c1e-122">"Microsoft. Compute/virtualMachines/\*" concede acesso a todas as operações de máquinas virtuais e seus tipos de recursos filhos.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="b9c1e-123">AssignableScopes: o conjunto de escopos (assinaturas do Azure ou grupos de recursos) em que a função personalizada estará disponível para a atribuição.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="b9c1e-124">Usando o AssignableScopes, você pode disponibilizar a função personalizada para atribuição somente em assinaturas ou grupos de recursos que precisarem, e não truncar a experiência do usuário para o restante das assinaturas ou grupos de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="b9c1e-125">Veja a seguir alguns escopos atribuíveis válidos:</span><span class="sxs-lookup"><span data-stu-id="b9c1e-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="b9c1e-126">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": torna a função disponível para a atribuição em duas assinaturas.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="b9c1e-127">"/subscriptions/c276fc76-9cd4-44C9-99a7-4fd71546436e": torna a função disponível para a atribuição em uma única assinatura.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="b9c1e-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": torna a função disponível para a atribuição somente no grupo de recursos de rede.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="b9c1e-129">A definição da função de entrada pode conter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="b9c1e-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="b9c1e-130">Ações: o conjunto de operações que devem ser excluídas das ações para determinar as ações efetivas para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="b9c1e-131">Se houver uma operação específica à qual você não deseja conceder acesso em uma função personalizada, é conveniente usar as ações para excluí-lo, em vez de especificar todas as operações que não sejam uma operação específica em ações.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="b9c1e-132">Dataactions: o conjunto de operações de dados às quais a função personalizada concede acesso.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="b9c1e-133">NotDataActions: o conjunto de operações que devem ser excluídas da dataactions para determinar as ações de dataacção efetivas para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective dataactions for the custom role.</span></span>
<span data-ttu-id="b9c1e-134">Se houver uma operação de dados específica para a qual você não deseja conceder acesso em uma função personalizada, é conveniente usar o NotDataActions para excluí-lo, em vez de especificar todas as operações que não sejam uma operação específica em ações.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="b9c1e-135">Observação: se um usuário é atribuído a uma função que especifica uma operação em minhas ações e também uma outra função concede acesso à mesma operação-o usuário poderá executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="b9c1e-136">Não é uma regra de negação-é simplesmente uma maneira conveniente de criar um conjunto de operações permitidas quando operações específicas precisam ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="b9c1e-137">Veja a seguir uma definição de função JSON de exemplo que pode ser fornecida como entrada {"nome": "função Updated", "Descrição": "pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "ações": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/reiniciar/ação", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]</span><span class="sxs-lookup"><span data-stu-id="b9c1e-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="b9c1e-138">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9c1e-138">EXAMPLES</span></span>

### <span data-ttu-id="b9c1e-139">Criar usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="b9c1e-139">Create using PSRoleDefinitionObject</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="b9c1e-140">Criar usando um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="b9c1e-140">Create using JSON file</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="b9c1e-141">OS</span><span class="sxs-lookup"><span data-stu-id="b9c1e-141">PARAMETERS</span></span>

### <span data-ttu-id="b9c1e-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c1e-142">-DefaultProfile</span></span>
<span data-ttu-id="b9c1e-143">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b9c1e-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9c1e-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b9c1e-144">-InputFile</span></span>
<span data-ttu-id="b9c1e-145">Nome do arquivo que contém uma única definição de função JSON.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="b9c1e-146">-Função</span><span class="sxs-lookup"><span data-stu-id="b9c1e-146">-Role</span></span>
<span data-ttu-id="b9c1e-147">Objeto de definição de função.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-147">Role definition object.</span></span>

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

### <span data-ttu-id="b9c1e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c1e-148">CommonParameters</span></span>
<span data-ttu-id="b9c1e-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c1e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c1e-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c1e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c1e-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9c1e-151">INPUTS</span></span>

### <span data-ttu-id="b9c1e-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b9c1e-152">None</span></span>

## <span data-ttu-id="b9c1e-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9c1e-153">OUTPUTS</span></span>

### <span data-ttu-id="b9c1e-154">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c1e-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="b9c1e-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9c1e-155">NOTES</span></span>
<span data-ttu-id="b9c1e-156">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="b9c1e-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b9c1e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9c1e-157">RELATED LINKS</span></span>

[<span data-ttu-id="b9c1e-158">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="b9c1e-158">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="b9c1e-159">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c1e-159">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="b9c1e-160">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c1e-160">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="b9c1e-161">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="b9c1e-161">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

