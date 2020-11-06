---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426610"
---
# <span data-ttu-id="23103-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="23103-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23103-102">SYNOPSIS</span></span>
<span data-ttu-id="23103-103">Modifica uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="23103-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="23103-104">Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="23103-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="23103-105">Primeiro, use o comando Get-AzureRmRoleDefinition para recuperar a função personalizada que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="23103-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="23103-106">Em seguida, modifique as propriedades que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="23103-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="23103-107">Por fim, salve a definição de função usando este comando.</span><span class="sxs-lookup"><span data-stu-id="23103-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23103-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23103-108">SYNTAX</span></span>

### <span data-ttu-id="23103-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="23103-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23103-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="23103-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23103-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23103-111">DESCRIPTION</span></span>
<span data-ttu-id="23103-112">O cmdlet Set-AzureRmRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="23103-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="23103-113">Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="23103-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="23103-114">A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="23103-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="23103-115">Não agir, dataactions, NotDataActions são opcionais.</span><span class="sxs-lookup"><span data-stu-id="23103-115">NotActions, DataActions, NotDataActions are optional.</span></span>

<span data-ttu-id="23103-116">Veja a seguir um exemplo de definição de função de JSON atualizado para Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="23103-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": "pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "ações": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] , "isactions": \[ "* /Write" \] , "dataactions": \[ "Microsoft. Storage/storageAccounts/blobservices/containers/BLOBs/ \] \[ contêineres/BLOBs/gravação" \] , "Microsoft. Storage/NotDataActions/blobservices/contêineres/BLOBs/gravação \[ \]</span><span class="sxs-lookup"><span data-stu-id="23103-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="23103-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23103-118">EXAMPLES</span></span>

### <span data-ttu-id="23103-119">Atualizar usando PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="23103-119">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="23103-120">Criar usando um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="23103-120">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="23103-121">OS</span><span class="sxs-lookup"><span data-stu-id="23103-121">PARAMETERS</span></span>

### <span data-ttu-id="23103-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23103-122">-DefaultProfile</span></span>
<span data-ttu-id="23103-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="23103-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23103-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="23103-124">-InputFile</span></span>
<span data-ttu-id="23103-125">Nome do arquivo que contém uma única definição de função JSON a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="23103-125">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="23103-126">Inclua apenas as propriedades que serão atualizadas no JSON.</span><span class="sxs-lookup"><span data-stu-id="23103-126">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="23103-127">A propriedade ID é necessária.</span><span class="sxs-lookup"><span data-stu-id="23103-127">Id property is Required.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23103-128">-Função</span><span class="sxs-lookup"><span data-stu-id="23103-128">-Role</span></span>
<span data-ttu-id="23103-129">Objeto de definição de função a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="23103-129">Role definition object to be updated</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23103-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23103-130">CommonParameters</span></span>
<span data-ttu-id="23103-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23103-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23103-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23103-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23103-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23103-133">INPUTS</span></span>

### <span data-ttu-id="23103-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-134">PSRoleDefinition</span></span>
<span data-ttu-id="23103-135">O parâmetro ' role ' aceita o valor do tipo ' PSRoleDefinition ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="23103-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="23103-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23103-136">OUTPUTS</span></span>

### <span data-ttu-id="23103-137">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="23103-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23103-138">NOTES</span></span>
<span data-ttu-id="23103-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="23103-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="23103-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23103-140">RELATED LINKS</span></span>

[<span data-ttu-id="23103-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="23103-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="23103-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="23103-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="23103-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="23103-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

