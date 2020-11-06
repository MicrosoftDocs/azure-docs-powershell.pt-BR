---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/New-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: 7ed4af8c6d5443c3cdc7c8ae395ecc66d0a927e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428415"
---
# <span data-ttu-id="8f7bb-101">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8f7bb-101">New-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="8f7bb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f7bb-103">Cria um conjunto de espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-103">Creates a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f7bb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f7bb-104">SYNTAX</span></span>

```
New-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f7bb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f7bb-105">DESCRIPTION</span></span>
<span data-ttu-id="8f7bb-106">O cmdlet **New-AzureRmPowerBIWorkspaceCollection** cria um conjunto do espaço de trabalho do Power bi para a sua assinatura do Azure no grupo de recursos e local especificados.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-106">The **New-AzureRmPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="8f7bb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f7bb-107">EXAMPLES</span></span>

### <span data-ttu-id="8f7bb-108">Exemplo 1: criar uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="8f7bb-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="8f7bb-109">Esse comando cria um conjunto de espaços de trabalho denominado WCN11 no grupo de recursos especificado no local especificado.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="8f7bb-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f7bb-110">PARAMETERS</span></span>

### <span data-ttu-id="8f7bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f7bb-111">-DefaultProfile</span></span>
<span data-ttu-id="8f7bb-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8f7bb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f7bb-113">-Local</span><span class="sxs-lookup"><span data-stu-id="8f7bb-113">-Location</span></span>
<span data-ttu-id="8f7bb-114">Especifica o local do Azure no qual esse cmdlet cria uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f7bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f7bb-116">Especifica o nome do grupo de recursos em que esse cmdlet cria uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="8f7bb-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="8f7bb-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="8f7bb-118">Especifica um nome para o conjunto do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-118">Specifies a name for the Power BI workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f7bb-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f7bb-119">-Confirm</span></span>
<span data-ttu-id="8f7bb-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f7bb-121">-WhatIf</span></span>
<span data-ttu-id="8f7bb-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f7bb-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f7bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f7bb-124">CommonParameters</span></span>
<span data-ttu-id="8f7bb-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f7bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f7bb-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f7bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f7bb-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f7bb-127">INPUTS</span></span>

### <span data-ttu-id="8f7bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8f7bb-128">System.String</span></span>

## <span data-ttu-id="8f7bb-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f7bb-129">OUTPUTS</span></span>

### <span data-ttu-id="8f7bb-130">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8f7bb-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="8f7bb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f7bb-131">NOTES</span></span>

## <span data-ttu-id="8f7bb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f7bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="8f7bb-133">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8f7bb-133">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="8f7bb-134">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="8f7bb-134">Remove-AzureRmPowerBIWorkspaceCollection</span></span>](./Remove-AzureRmPowerBIWorkspaceCollection.md)


