---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946272"
---
# <span data-ttu-id="77dd6-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="77dd6-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="77dd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="77dd6-103">Obtém todos os locais de site disponíveis.</span><span class="sxs-lookup"><span data-stu-id="77dd6-103">Gets all available website locations.</span></span>

## <span data-ttu-id="77dd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77dd6-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77dd6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="77dd6-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77dd6-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="77dd6-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="77dd6-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="77dd6-108">Obtém todos os locais de site disponíveis para a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="77dd6-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="77dd6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77dd6-109">EXAMPLES</span></span>

### <span data-ttu-id="77dd6-110">Exemplo 1: obter todos os locais disponíveis</span><span class="sxs-lookup"><span data-stu-id="77dd6-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="77dd6-111">Este exemplo obtém todos os locais de site disponíveis para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="77dd6-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="77dd6-112">OS</span><span class="sxs-lookup"><span data-stu-id="77dd6-112">PARAMETERS</span></span>

### <span data-ttu-id="77dd6-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="77dd6-113">-Profile</span></span>
<span data-ttu-id="77dd6-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="77dd6-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77dd6-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="77dd6-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77dd6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77dd6-116">CommonParameters</span></span>
<span data-ttu-id="77dd6-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77dd6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77dd6-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77dd6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77dd6-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77dd6-119">INPUTS</span></span>

## <span data-ttu-id="77dd6-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77dd6-120">OUTPUTS</span></span>

## <span data-ttu-id="77dd6-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77dd6-121">NOTES</span></span>

## <span data-ttu-id="77dd6-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77dd6-122">RELATED LINKS</span></span>

[<span data-ttu-id="77dd6-123">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="77dd6-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


