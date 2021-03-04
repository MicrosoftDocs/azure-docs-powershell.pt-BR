---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887856"
---
# <span data-ttu-id="4f0db-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="4f0db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f0db-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0db-103">Modifica uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="4f0db-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="4f0db-104">Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="4f0db-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="4f0db-105">Primeiro, use o comando Get-AzRoleDefinition para recuperar a função personalizada que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="4f0db-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="4f0db-106">Em seguida, modifique as propriedades que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="4f0db-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="4f0db-107">Por fim, salve a definição de função usando este comando.</span><span class="sxs-lookup"><span data-stu-id="4f0db-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="4f0db-108">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4f0db-108">SYNTAX</span></span>

### <span data-ttu-id="4f0db-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f0db-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f0db-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f0db-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f0db-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f0db-111">DESCRIPTION</span></span>
<span data-ttu-id="4f0db-112">O Set-AzRoleDefinition cmdlet atualiza uma função personalizada existente no Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="4f0db-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="4f0db-113">Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="4f0db-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="4f0db-114">A definição de função para a função personalizada atualizada DEVE conter a ID e todas as outras propriedades necessárias da função, mesmo que não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="4f0db-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="4f0db-115">NotActions, DataActions, NotDataActions são opcionais.</span><span class="sxs-lookup"><span data-stu-id="4f0db-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="4f0db-116">A seguir está um exemplo de definição de função atualizada json para Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Ações": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="4f0db-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="4f0db-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f0db-117">EXAMPLES</span></span>

### <span data-ttu-id="4f0db-118">Exemplo 1: atualização usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="4f0db-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="4f0db-119">Exemplo 2: Criar usando o arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="4f0db-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="4f0db-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4f0db-120">PARAMETERS</span></span>

### <span data-ttu-id="4f0db-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0db-121">-DefaultProfile</span></span>
<span data-ttu-id="4f0db-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4f0db-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f0db-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4f0db-123">-InputFile</span></span>
<span data-ttu-id="4f0db-124">Nome do arquivo que contém uma única definição de função json a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="4f0db-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="4f0db-125">Inclua apenas as propriedades que devem ser atualizadas no JSON.</span><span class="sxs-lookup"><span data-stu-id="4f0db-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="4f0db-126">A propriedade Id é Obrigatório.</span><span class="sxs-lookup"><span data-stu-id="4f0db-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f0db-127">-Role</span><span class="sxs-lookup"><span data-stu-id="4f0db-127">-Role</span></span>
<span data-ttu-id="4f0db-128">Objeto de definição de função a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="4f0db-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f0db-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0db-129">CommonParameters</span></span>
<span data-ttu-id="4f0db-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f0db-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0db-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f0db-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0db-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f0db-132">INPUTS</span></span>

### <span data-ttu-id="4f0db-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="4f0db-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4f0db-134">OUTPUTS</span></span>

### <span data-ttu-id="4f0db-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="4f0db-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="4f0db-136">NOTES</span></span>
<span data-ttu-id="4f0db-137">Palavras-chave: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="4f0db-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4f0db-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f0db-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f0db-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="4f0db-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="4f0db-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="4f0db-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="4f0db-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="4f0db-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

