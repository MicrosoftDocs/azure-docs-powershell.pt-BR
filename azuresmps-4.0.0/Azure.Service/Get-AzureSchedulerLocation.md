---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 410A58A3-CB0E-43FE-B490-B1520BD1CCEC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c445e2b42738f288de960f30f4c98d909c71784
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945611"
---
# <span data-ttu-id="e084e-101">Get-AzureSchedulerLocation</span><span class="sxs-lookup"><span data-stu-id="e084e-101">Get-AzureSchedulerLocation</span></span>

## <span data-ttu-id="e084e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e084e-102">SYNOPSIS</span></span>
<span data-ttu-id="e084e-103">Obtém locais do Agendador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e084e-103">Gets available scheduler locations.</span></span>

## <span data-ttu-id="e084e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e084e-104">SYNTAX</span></span>

```
Get-AzureSchedulerLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e084e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e084e-105">DESCRIPTION</span></span>
<span data-ttu-id="e084e-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e084e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e084e-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e084e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e084e-108">O cmdlet **Get-AzureSchedulerLocation** Obtém locais do Agendador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e084e-108">The **Get-AzureSchedulerLocation** cmdlet gets available scheduler locations.</span></span>

## <span data-ttu-id="e084e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e084e-109">EXAMPLES</span></span>

### <span data-ttu-id="e084e-110">Exemplo 1: obter locais do Agendador disponíveis</span><span class="sxs-lookup"><span data-stu-id="e084e-110">Example 1: Get available scheduler locations</span></span>
```
PS C:\> Get-AzureSchedulerLocation
```

<span data-ttu-id="e084e-111">Esse comando obtém locais do Agendador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e084e-111">This command gets available scheduler locations.</span></span>

## <span data-ttu-id="e084e-112">OS</span><span class="sxs-lookup"><span data-stu-id="e084e-112">PARAMETERS</span></span>

### <span data-ttu-id="e084e-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e084e-113">-Profile</span></span>
<span data-ttu-id="e084e-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e084e-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e084e-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e084e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e084e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e084e-116">CommonParameters</span></span>
<span data-ttu-id="e084e-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e084e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e084e-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e084e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e084e-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e084e-119">INPUTS</span></span>

## <span data-ttu-id="e084e-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e084e-120">OUTPUTS</span></span>

## <span data-ttu-id="e084e-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e084e-121">NOTES</span></span>

## <span data-ttu-id="e084e-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e084e-122">RELATED LINKS</span></span>

[<span data-ttu-id="e084e-123">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="e084e-123">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="e084e-124">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="e084e-124">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="e084e-125">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="e084e-125">Get-AzureSchedulerJobHistory</span></span>](./Get-AzureSchedulerJobHistory.md)


