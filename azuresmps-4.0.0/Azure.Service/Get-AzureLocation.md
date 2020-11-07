---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946336"
---
# <span data-ttu-id="e5675-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="e5675-101">Get-AzureLocation</span></span>

## <span data-ttu-id="e5675-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5675-102">SYNOPSIS</span></span>
<span data-ttu-id="e5675-103">Obtém os locais de centro de dados disponíveis para a assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5675-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="e5675-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5675-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e5675-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5675-105">DESCRIPTION</span></span>
<span data-ttu-id="e5675-106">O cmdlet **Get-AzureLocation** Obtém uma lista dos data centers do Azure disponíveis e suas propriedades para a assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="e5675-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="e5675-107">Antes de executar este cmdlet, você deve definir sua assinatura atual usando os cmdlets Select-AzureSubscription e Set-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="e5675-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="e5675-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5675-108">EXAMPLES</span></span>

### <span data-ttu-id="e5675-109">Exemplo 1: obter locais</span><span class="sxs-lookup"><span data-stu-id="e5675-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="e5675-110">Esse comando obtém uma lista de centros de dados disponíveis e suas propriedades para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e5675-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="e5675-111">OS</span><span class="sxs-lookup"><span data-stu-id="e5675-111">PARAMETERS</span></span>

### <span data-ttu-id="e5675-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e5675-112">-InformationAction</span></span>
<span data-ttu-id="e5675-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e5675-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e5675-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e5675-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e5675-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e5675-115">Continue</span></span>
- <span data-ttu-id="e5675-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e5675-116">Ignore</span></span>
- <span data-ttu-id="e5675-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="e5675-117">Inquire</span></span>
- <span data-ttu-id="e5675-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e5675-118">SilentlyContinue</span></span>
- <span data-ttu-id="e5675-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e5675-119">Stop</span></span>
- <span data-ttu-id="e5675-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e5675-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5675-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e5675-121">-InformationVariable</span></span>
<span data-ttu-id="e5675-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e5675-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5675-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e5675-123">-Profile</span></span>
<span data-ttu-id="e5675-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e5675-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e5675-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e5675-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e5675-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5675-126">CommonParameters</span></span>
<span data-ttu-id="e5675-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5675-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5675-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5675-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5675-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5675-129">INPUTS</span></span>

## <span data-ttu-id="e5675-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5675-130">OUTPUTS</span></span>

## <span data-ttu-id="e5675-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5675-131">NOTES</span></span>

## <span data-ttu-id="e5675-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5675-132">RELATED LINKS</span></span>

