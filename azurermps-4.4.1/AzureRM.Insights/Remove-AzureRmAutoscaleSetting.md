---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433119"
---
# <span data-ttu-id="00368-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="00368-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="00368-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00368-102">SYNOPSIS</span></span>
<span data-ttu-id="00368-103">Remove uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="00368-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00368-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00368-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00368-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00368-105">DESCRIPTION</span></span>
<span data-ttu-id="00368-106">O cmdlet **Remove-AzureRmAutoscaleSetting** remove uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="00368-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="00368-107">Você deve especificar o nome da configuração e o nome do grupo de recursos ao qual ele está atribuído.</span><span class="sxs-lookup"><span data-stu-id="00368-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="00368-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00368-108">EXAMPLES</span></span>

## <span data-ttu-id="00368-109">OS</span><span class="sxs-lookup"><span data-stu-id="00368-109">PARAMETERS</span></span>

### <span data-ttu-id="00368-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="00368-110">-Name</span></span>
<span data-ttu-id="00368-111">Especifica o nome da configuração de dimensionamento automático a ser removida.</span><span class="sxs-lookup"><span data-stu-id="00368-111">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="00368-112">-Resource</span><span class="sxs-lookup"><span data-stu-id="00368-112">-ResourceGroup</span></span>
<span data-ttu-id="00368-113">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="00368-113">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="00368-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00368-114">-DefaultProfile</span></span>
<span data-ttu-id="00368-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00368-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00368-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00368-116">CommonParameters</span></span>
<span data-ttu-id="00368-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00368-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00368-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00368-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00368-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00368-119">INPUTS</span></span>

## <span data-ttu-id="00368-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00368-120">OUTPUTS</span></span>

### <span data-ttu-id="00368-121">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="00368-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="00368-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00368-122">NOTES</span></span>

## <span data-ttu-id="00368-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00368-123">RELATED LINKS</span></span>

[<span data-ttu-id="00368-124">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="00368-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="00368-125">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="00368-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


