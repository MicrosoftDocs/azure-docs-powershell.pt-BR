---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433121"
---
# <span data-ttu-id="f9a62-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a62-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="f9a62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9a62-102">SYNOPSIS</span></span>
<span data-ttu-id="f9a62-103">Remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="f9a62-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9a62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9a62-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9a62-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9a62-105">DESCRIPTION</span></span>
<span data-ttu-id="f9a62-106">O cmdlet **Remove-AzureRmAlertRule** remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="f9a62-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="f9a62-107">Você deve especificar o nome da regra de alerta e o grupo de recursos ao qual ele está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f9a62-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="f9a62-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9a62-108">EXAMPLES</span></span>

### <span data-ttu-id="f9a62-109">Exemplo 1: remover uma regra de alerta</span><span class="sxs-lookup"><span data-stu-id="f9a62-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="f9a62-110">Esse comando Remove a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8 no grupo de recursos Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="f9a62-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="f9a62-111">OS</span><span class="sxs-lookup"><span data-stu-id="f9a62-111">PARAMETERS</span></span>

### <span data-ttu-id="f9a62-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9a62-112">-Name</span></span>
<span data-ttu-id="f9a62-113">Especifica o nome da regra de alerta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f9a62-113">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a62-114">-Resource</span><span class="sxs-lookup"><span data-stu-id="f9a62-114">-ResourceGroup</span></span>
<span data-ttu-id="f9a62-115">Especifica o nome do grupo de recursos para a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="f9a62-115">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9a62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9a62-116">-DefaultProfile</span></span>
<span data-ttu-id="f9a62-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9a62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9a62-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9a62-118">CommonParameters</span></span>
<span data-ttu-id="f9a62-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9a62-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9a62-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9a62-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9a62-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9a62-121">INPUTS</span></span>

## <span data-ttu-id="f9a62-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9a62-122">OUTPUTS</span></span>

### <span data-ttu-id="f9a62-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="f9a62-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="f9a62-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9a62-124">NOTES</span></span>

## <span data-ttu-id="f9a62-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9a62-125">RELATED LINKS</span></span>

[<span data-ttu-id="f9a62-126">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a62-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="f9a62-127">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a62-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="f9a62-128">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a62-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f9a62-129">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f9a62-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="f9a62-130">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f9a62-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


