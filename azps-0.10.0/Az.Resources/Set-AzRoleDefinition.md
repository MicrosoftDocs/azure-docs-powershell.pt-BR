---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 79ff5a54da704e66895e280c8a2e8a93731d2083
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776310"
---
# <span data-ttu-id="9613c-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="9613c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9613c-102">SYNOPSIS</span></span>
<span data-ttu-id="9613c-103">Modifica uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="9613c-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="9613c-104">Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="9613c-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="9613c-105">Primeiro, use o comando Get-AzRoleDefinition para recuperar a função personalizada que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="9613c-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="9613c-106">Em seguida, modifique as propriedades que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="9613c-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="9613c-107">Por fim, salve a definição de função usando este comando.</span><span class="sxs-lookup"><span data-stu-id="9613c-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="9613c-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9613c-108">SYNTAX</span></span>

### <span data-ttu-id="9613c-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="9613c-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9613c-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="9613c-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9613c-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9613c-111">DESCRIPTION</span></span>
<span data-ttu-id="9613c-112">O cmdlet Set-AzRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="9613c-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="9613c-113">Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="9613c-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="9613c-114">A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="9613c-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="9613c-115">Não agir, dataactions, NotDataActions são opcionais.</span><span class="sxs-lookup"><span data-stu-id="9613c-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="9613c-116">Veja a seguir um exemplo de definição de função em JSON para Set-AzRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": " \[ *Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "/Read", "Microsoft.//Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]</span><span class="sxs-lookup"><span data-stu-id="9613c-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="9613c-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9613c-117">EXAMPLES</span></span>

### <span data-ttu-id="9613c-118">Atualizar usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="9613c-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="9613c-119">Criar usando um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="9613c-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="9613c-120">OS</span><span class="sxs-lookup"><span data-stu-id="9613c-120">PARAMETERS</span></span>

### <span data-ttu-id="9613c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9613c-121">-DefaultProfile</span></span>
<span data-ttu-id="9613c-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9613c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9613c-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="9613c-123">-InputFile</span></span>
<span data-ttu-id="9613c-124">Nome do arquivo que contém uma única definição de função JSON a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="9613c-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="9613c-125">Inclua apenas as propriedades que serão atualizadas no JSON.</span><span class="sxs-lookup"><span data-stu-id="9613c-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="9613c-126">A propriedade ID é necessária.</span><span class="sxs-lookup"><span data-stu-id="9613c-126">Id property is Required.</span></span>

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

### <span data-ttu-id="9613c-127">-Função</span><span class="sxs-lookup"><span data-stu-id="9613c-127">-Role</span></span>
<span data-ttu-id="9613c-128">Objeto de definição de função a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="9613c-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="9613c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9613c-129">CommonParameters</span></span>
<span data-ttu-id="9613c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9613c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9613c-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9613c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9613c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9613c-132">INPUTS</span></span>

### <span data-ttu-id="9613c-133">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="9613c-134">Parâmetros: Role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9613c-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="9613c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9613c-135">OUTPUTS</span></span>

### <span data-ttu-id="9613c-136">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="9613c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9613c-137">NOTES</span></span>
<span data-ttu-id="9613c-138">Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="9613c-138">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9613c-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9613c-139">RELATED LINKS</span></span>

[<span data-ttu-id="9613c-140">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="9613c-140">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="9613c-141">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-141">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="9613c-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="9613c-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="9613c-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

