---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114073"
---
# <span data-ttu-id="3ccb8-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="3ccb8-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="3ccb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ccb8-102">SYNOPSIS</span></span>
<span data-ttu-id="3ccb8-103">Obtém as chaves compartilhadas de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="3ccb8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ccb8-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ccb8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ccb8-105">DESCRIPTION</span></span>
<span data-ttu-id="3ccb8-106">O **cmdlet Get-AzOperationalInsightsWorkspaceSharedKey** lista as chaves compartilhadas de um espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="3ccb8-107">As teclas são usadas para conectar os agentes do Insights Operacionais ao espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="3ccb8-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ccb8-108">EXAMPLES</span></span>

### <span data-ttu-id="3ccb8-109">Exemplo 1: Obter chaves compartilhadas por nome de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="3ccb8-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="3ccb8-110">Esse comando obtém as chaves compartilhadas do espaço de trabalho chamado MyWorkspace no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="3ccb8-111">Exemplo 2: Obter chaves compartilhadas usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="3ccb8-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="3ccb8-112">Esse comando obtém o espaço de trabalho chamado MyWorkspace usando o cmdlet Get-AzOperationalInsightsWorkspace e passa o espaço de trabalho para o cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey.**</span><span class="sxs-lookup"><span data-stu-id="3ccb8-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="3ccb8-113">O comando obtém as chaves compartilhadas para esse espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="3ccb8-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ccb8-114">PARAMETERS</span></span>

### <span data-ttu-id="3ccb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ccb8-115">-DefaultProfile</span></span>
<span data-ttu-id="3ccb8-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3ccb8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ccb8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ccb8-117">-Name</span></span>
<span data-ttu-id="3ccb8-118">Especifica o nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ccb8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ccb8-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ccb8-120">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="3ccb8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ccb8-121">CommonParameters</span></span>
<span data-ttu-id="3ccb8-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ccb8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ccb8-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ccb8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ccb8-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ccb8-124">INPUTS</span></span>

### <span data-ttu-id="3ccb8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="3ccb8-125">System.String</span></span>

## <span data-ttu-id="3ccb8-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ccb8-126">OUTPUTS</span></span>

### <span data-ttu-id="3ccb8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="3ccb8-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="3ccb8-128">Notas</span><span class="sxs-lookup"><span data-stu-id="3ccb8-128">NOTES</span></span>

## <span data-ttu-id="3ccb8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ccb8-129">RELATED LINKS</span></span>

[<span data-ttu-id="3ccb8-130">Cmdlets de Insights Operacionais do Azure</span><span class="sxs-lookup"><span data-stu-id="3ccb8-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="3ccb8-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ccb8-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


