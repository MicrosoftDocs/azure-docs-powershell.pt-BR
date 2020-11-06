---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: EEF32F48-00F6-4C57-B4F1-B58B566EAFEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: f00ddaade85ba981fa19209df5efb3a96160b410
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602250"
---
# <span data-ttu-id="85e0f-101">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85e0f-101">Get-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="85e0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="85e0f-103">Obtém as coleções do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="85e0f-103">Gets Power BI workspace collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85e0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85e0f-104">SYNTAX</span></span>

### <span data-ttu-id="85e0f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e0f-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85e0f-106">WorkspaceCollectionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85e0f-106">WorkspaceCollectionNameParameterSet</span></span>
```
Get-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85e0f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="85e0f-108">O cmdlet **Get-AzureRmPowerBIWorkspaceCollection** Obtém as coleções do espaço de trabalho do Power bi e seu grupo de recursos do Azure, ou pelo nome da coleção.</span><span class="sxs-lookup"><span data-stu-id="85e0f-108">The **Get-AzureRmPowerBIWorkspaceCollection** cmdlet gets Power BI workspace collections in your Azure subscription and resource group, or by collection name.</span></span>

## <span data-ttu-id="85e0f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85e0f-109">EXAMPLES</span></span>

### <span data-ttu-id="85e0f-110">Exemplo 1: obter todas as coleções do espaço de trabalho em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="85e0f-110">Example 1: Get all workspace collections in a resource group</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17"
```

<span data-ttu-id="85e0f-111">Esse comando obtém as coleções do espaço de trabalho que pertencem ao grupo de recursos chamado ResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="85e0f-111">This command gets the workspace collections that belong to the resource group named ResourceGroup17.</span></span>

### <span data-ttu-id="85e0f-112">Exemplo 2: obter uma coleção de espaço de trabalho usando seu nome</span><span class="sxs-lookup"><span data-stu-id="85e0f-112">Example 2: Get a workspace collection by using its name</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="85e0f-113">Esse comando obtém a coleção de espaço de trabalho chamada WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="85e0f-113">This command gets the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="85e0f-114">OS</span><span class="sxs-lookup"><span data-stu-id="85e0f-114">PARAMETERS</span></span>

### <span data-ttu-id="85e0f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e0f-115">-DefaultProfile</span></span>
<span data-ttu-id="85e0f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="85e0f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85e0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85e0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="85e0f-118">Especifica o nome do grupo de recursos a partir do qual esse cmdlet obtém coleções do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="85e0f-118">Specifies the name of the resource group from which this cmdlet gets workspace collections.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e0f-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="85e0f-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="85e0f-120">Especifica o nome da coleção do espaço de trabalho do Power BI que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="85e0f-120">Specifies the name of the Power BI workspace collection that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: WorkspaceCollectionNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85e0f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e0f-121">CommonParameters</span></span>
<span data-ttu-id="85e0f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e0f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e0f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85e0f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e0f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85e0f-124">INPUTS</span></span>

### <span data-ttu-id="85e0f-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85e0f-125">None</span></span>
<span data-ttu-id="85e0f-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="85e0f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85e0f-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85e0f-127">OUTPUTS</span></span>

### <span data-ttu-id="85e0f-128">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85e0f-128">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="85e0f-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85e0f-129">NOTES</span></span>

## <span data-ttu-id="85e0f-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85e0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="85e0f-131">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85e0f-131">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="85e0f-132">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="85e0f-132">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


