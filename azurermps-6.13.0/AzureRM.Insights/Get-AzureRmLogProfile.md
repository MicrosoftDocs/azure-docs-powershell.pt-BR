---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440792"
---
# <span data-ttu-id="874f4-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="874f4-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="874f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="874f4-102">SYNOPSIS</span></span>
<span data-ttu-id="874f4-103">Obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="874f4-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="874f4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="874f4-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="874f4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="874f4-105">DESCRIPTION</span></span>
<span data-ttu-id="874f4-106">O cmdlet **Get-AzureRmLogProfile** Obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="874f4-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="874f4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="874f4-107">EXAMPLES</span></span>

## <span data-ttu-id="874f4-108">OS</span><span class="sxs-lookup"><span data-stu-id="874f4-108">PARAMETERS</span></span>

### <span data-ttu-id="874f4-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874f4-109">-DefaultProfile</span></span>
<span data-ttu-id="874f4-110">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="874f4-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="874f4-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="874f4-111">-Name</span></span>
<span data-ttu-id="874f4-112">Especifica o nome do perfil de log a obter.</span><span class="sxs-lookup"><span data-stu-id="874f4-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="874f4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874f4-113">CommonParameters</span></span>
<span data-ttu-id="874f4-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="874f4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874f4-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="874f4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874f4-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="874f4-116">INPUTS</span></span>

### <span data-ttu-id="874f4-117">System. String</span><span class="sxs-lookup"><span data-stu-id="874f4-117">System.String</span></span>

## <span data-ttu-id="874f4-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="874f4-118">OUTPUTS</span></span>

### <span data-ttu-id="874f4-119">Microsoft. Azure. Commands. insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="874f4-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="874f4-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="874f4-120">NOTES</span></span>

## <span data-ttu-id="874f4-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="874f4-121">RELATED LINKS</span></span>

[<span data-ttu-id="874f4-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="874f4-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="874f4-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="874f4-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


