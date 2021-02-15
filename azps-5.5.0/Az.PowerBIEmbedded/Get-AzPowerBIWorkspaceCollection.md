---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: d3be067690b755014fe02840d355fc36e0d6aa20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112708"
---
# <span data-ttu-id="64aa5-101">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="64aa5-101">Get-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="64aa5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="64aa5-103">Obtém coleções de espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="64aa5-103">Gets Power BI workspace collections.</span></span>

## <span data-ttu-id="64aa5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64aa5-104">SYNTAX</span></span>

### <span data-ttu-id="64aa5-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="64aa5-105">ResourceGroupParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64aa5-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="64aa5-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64aa5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="64aa5-107">DESCRIPTION</span></span>
<span data-ttu-id="64aa5-108">O cmdlet **Get-AzPowerBIWorkspaceCollection** obtém coleções de espaço de trabalho do Power BI em sua assinatura do Azure e grupo de recursos, ou por nome de coleção.</span><span class="sxs-lookup"><span data-stu-id="64aa5-108">The **Get-AzPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="64aa5-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="64aa5-109">EXAMPLES</span></span>

### <span data-ttu-id="64aa5-110">Exemplo 1: Obter todas as coleções de espaço de trabalho em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64aa5-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="64aa5-111">Esse comando obtém as coleções de espaço de trabalho que pertencem ao grupo de recursos chamado ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="64aa5-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="64aa5-112">Exemplo 2: Obter um conjunto de espaços de trabalho usando seu nome</span><span class="sxs-lookup"><span data-stu-id="64aa5-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="64aa5-113">Esse comando obtém o conjunto de espaços de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="64aa5-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="64aa5-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64aa5-114">PARAMETERS</span></span>

### <span data-ttu-id="64aa5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64aa5-115">-DefaultProfile</span></span>
<span data-ttu-id="64aa5-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="64aa5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64aa5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64aa5-117">-ResourceGroupName</span></span>
<span data-ttu-id="64aa5-118">Especifica o nome do grupo de recursos do qual este cmdlet obtém coleções de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="64aa5-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aa5-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="64aa5-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="64aa5-120">Especifica o nome da coleção de espaços de trabalho do Power BI que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="64aa5-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64aa5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64aa5-121">CommonParameters</span></span>
<span data-ttu-id="64aa5-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64aa5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64aa5-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64aa5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64aa5-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="64aa5-124">INPUTS</span></span>

### <span data-ttu-id="64aa5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="64aa5-125">System.String</span></span>

## <span data-ttu-id="64aa5-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="64aa5-126">OUTPUTS</span></span>

### <span data-ttu-id="64aa5-127">Microsoft.Azure.Commands.Management.PowerBIEmbeed.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="64aa5-127">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="64aa5-128">Notas</span><span class="sxs-lookup"><span data-stu-id="64aa5-128">NOTES</span></span>

## <span data-ttu-id="64aa5-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64aa5-129">RELATED LINKS</span></span>

[<span data-ttu-id="64aa5-130">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="64aa5-130">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="64aa5-131">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="64aa5-131">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


