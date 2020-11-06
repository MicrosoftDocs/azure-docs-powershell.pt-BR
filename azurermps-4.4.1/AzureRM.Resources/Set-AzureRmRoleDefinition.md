---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430663"
---
# <span data-ttu-id="95542-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="95542-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95542-102">SYNOPSIS</span></span>
<span data-ttu-id="95542-103">Modifica uma função personalizada no Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="95542-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="95542-104">Forneça a definição de função modificada como um arquivo JSON ou como um PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="95542-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="95542-105">Primeiro, use o comando Get-AzureRmRoleDefinition para recuperar a função personalizada que você deseja modificar.</span><span class="sxs-lookup"><span data-stu-id="95542-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="95542-106">Em seguida, modifique as propriedades que você deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="95542-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="95542-107">Por fim, salve a definição de função usando este comando.</span><span class="sxs-lookup"><span data-stu-id="95542-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95542-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95542-108">SYNTAX</span></span>

### <span data-ttu-id="95542-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="95542-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95542-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="95542-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95542-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95542-111">DESCRIPTION</span></span>
<span data-ttu-id="95542-112">O cmdlet Set-AzureRmRoleDefinition atualiza uma função personalizada existente no controle de acesso do Azure Role-Based.</span><span class="sxs-lookup"><span data-stu-id="95542-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="95542-113">Forneça a definição de função atualizada como uma entrada para o comando como um arquivo JSON ou um objeto PSRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="95542-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="95542-114">A definição de função para a função personalizada atualizada deve conter a ID e todas as outras propriedades necessárias da função, mesmo que elas não sejam atualizadas: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="95542-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="95542-115">Ação é opcional.</span><span class="sxs-lookup"><span data-stu-id="95542-115">NotActions is optional.</span></span>

<span data-ttu-id="95542-116">Veja a seguir um exemplo de definição de função de JSON atualizado para Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="95542-117">{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "nome": "função Updated", "Descrição": "pode monitorar todos os recursos e iniciar e reiniciar máquinas virtuais", "ações": \[ "\*/Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Action", "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] "AssignableScopes": \[ "/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }</span><span class="sxs-lookup"><span data-stu-id="95542-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "\*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] "AssignableScopes": \["/subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f"\] }</span></span>

## <span data-ttu-id="95542-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95542-118">EXAMPLES</span></span>

### <span data-ttu-id="95542-119">Atualização--------------------------usando PSRoleDefinitionObject--------------------------</span><span class="sxs-lookup"><span data-stu-id="95542-119">--------------------------  Update using PSRoleDefinitionObject  --------------------------</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="95542-120">--------------------------Criar usando o arquivo JSON--------------------------</span><span class="sxs-lookup"><span data-stu-id="95542-120">--------------------------  Create using JSON file  --------------------------</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="95542-121">OS</span><span class="sxs-lookup"><span data-stu-id="95542-121">PARAMETERS</span></span>

### <span data-ttu-id="95542-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="95542-122">-InputFile</span></span>
<span data-ttu-id="95542-123">Nome do arquivo que contém uma única definição de função JSON a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="95542-123">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="95542-124">Inclua apenas as propriedades que serão atualizadas no JSON.</span><span class="sxs-lookup"><span data-stu-id="95542-124">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="95542-125">A propriedade ID é necessária.</span><span class="sxs-lookup"><span data-stu-id="95542-125">Id property is Required.</span></span>

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

### <span data-ttu-id="95542-126">-Função</span><span class="sxs-lookup"><span data-stu-id="95542-126">-Role</span></span>
<span data-ttu-id="95542-127">Objeto de definição de função a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="95542-127">Role definition object to be updated</span></span>

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

### <span data-ttu-id="95542-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95542-128">-DefaultProfile</span></span>
<span data-ttu-id="95542-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95542-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95542-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95542-130">CommonParameters</span></span>
<span data-ttu-id="95542-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95542-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95542-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95542-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95542-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95542-133">INPUTS</span></span>

### <span data-ttu-id="95542-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-134">PSRoleDefinition</span></span>
<span data-ttu-id="95542-135">O parâmetro ' role ' aceita o valor do tipo ' PSRoleDefinition ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="95542-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="95542-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95542-136">OUTPUTS</span></span>

### <span data-ttu-id="95542-137">Microsoft. Azure. Commands. Resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="95542-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95542-138">NOTES</span></span>
<span data-ttu-id="95542-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="95542-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="95542-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95542-140">RELATED LINKS</span></span>

[<span data-ttu-id="95542-141">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="95542-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="95542-142">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="95542-143">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="95542-144">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="95542-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

