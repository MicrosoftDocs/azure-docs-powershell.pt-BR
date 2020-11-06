---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Remove-AzureRmPowerBIWorkspaceCollection.md
ms.openlocfilehash: c377beb022b3d44d8b96a560c4bdd8b0c6daa387
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610484"
---
# <span data-ttu-id="7724a-101">Remove-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7724a-101">Remove-AzureRmPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="7724a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7724a-102">SYNOPSIS</span></span>
<span data-ttu-id="7724a-103">Remove um conjunto do espaço de trabalho do Power BI.</span><span class="sxs-lookup"><span data-stu-id="7724a-103">Removes a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7724a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7724a-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7724a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7724a-105">DESCRIPTION</span></span>
<span data-ttu-id="7724a-106">O cmdlet **Remove-AzureRmPowerBIWorkspaceCollection** remove uma coleção de espaço de trabalho do Power bi de sua assinatura do Azure e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7724a-106">The **Remove-AzureRmPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="7724a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7724a-107">EXAMPLES</span></span>

### <span data-ttu-id="7724a-108">Exemplo 1: remover uma coleção de espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="7724a-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzureRmPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="7724a-109">Esse comando Remove a coleção do espaço de trabalho chamado WCN11 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7724a-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="7724a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7724a-110">PARAMETERS</span></span>

### <span data-ttu-id="7724a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7724a-111">-ResourceGroupName</span></span>
<span data-ttu-id="7724a-112">Especifica o nome do grupo de recursos do qual esse cmdlet Remove uma coleção de espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7724a-112">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="7724a-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="7724a-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="7724a-114">Especifica o nome da coleção do espaço de trabalho do Power BI que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="7724a-114">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7724a-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7724a-115">-Confirm</span></span>
<span data-ttu-id="7724a-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7724a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7724a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7724a-117">-WhatIf</span></span>
<span data-ttu-id="7724a-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7724a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7724a-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7724a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7724a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7724a-120">-DefaultProfile</span></span>
<span data-ttu-id="7724a-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7724a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7724a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7724a-122">CommonParameters</span></span>
<span data-ttu-id="7724a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7724a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7724a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7724a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7724a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7724a-125">INPUTS</span></span>

## <span data-ttu-id="7724a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7724a-126">OUTPUTS</span></span>

## <span data-ttu-id="7724a-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7724a-127">NOTES</span></span>

## <span data-ttu-id="7724a-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7724a-128">RELATED LINKS</span></span>

[<span data-ttu-id="7724a-129">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7724a-129">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)

[<span data-ttu-id="7724a-130">New-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="7724a-130">New-AzureRmPowerBIWorkspaceCollection</span></span>](./New-AzureRmPowerBIWorkspaceCollection.md)


