---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 846B9EB8-8EC2-4BDA-90EF-59098696F460
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c4e1dedb02286ceaab182e0912198c23ec03ee5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945793"
---
# <span data-ttu-id="3017c-101">Set-AzureVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3017c-101">Set-AzureVMBootDiagnostics</span></span>

## <span data-ttu-id="3017c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3017c-102">SYNOPSIS</span></span>

## <span data-ttu-id="3017c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3017c-103">SYNTAX</span></span>

### <span data-ttu-id="3017c-104">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3017c-104">EnableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Enable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3017c-105">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="3017c-105">DisableBootDiagnostics</span></span>
```
Set-AzureVMBootDiagnostics [-Disable] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3017c-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3017c-106">DESCRIPTION</span></span>

## <span data-ttu-id="3017c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3017c-107">EXAMPLES</span></span>

### <span data-ttu-id="3017c-108">1:</span><span class="sxs-lookup"><span data-stu-id="3017c-108">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3017c-109">OS</span><span class="sxs-lookup"><span data-stu-id="3017c-109">PARAMETERS</span></span>

### <span data-ttu-id="3017c-110">-Disable</span><span class="sxs-lookup"><span data-stu-id="3017c-110">-Disable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3017c-111">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="3017c-111">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3017c-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3017c-112">-InformationAction</span></span>
<span data-ttu-id="3017c-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="3017c-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3017c-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3017c-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3017c-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="3017c-115">Continue</span></span>
- <span data-ttu-id="3017c-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="3017c-116">Ignore</span></span>
- <span data-ttu-id="3017c-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="3017c-117">Inquire</span></span>
- <span data-ttu-id="3017c-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3017c-118">SilentlyContinue</span></span>
- <span data-ttu-id="3017c-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="3017c-119">Stop</span></span>
- <span data-ttu-id="3017c-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="3017c-120">Suspend</span></span>

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

### <span data-ttu-id="3017c-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3017c-121">-InformationVariable</span></span>
<span data-ttu-id="3017c-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="3017c-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3017c-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3017c-123">-Profile</span></span>
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

### <span data-ttu-id="3017c-124">-VM</span><span class="sxs-lookup"><span data-stu-id="3017c-124">-VM</span></span>
```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3017c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3017c-125">CommonParameters</span></span>
<span data-ttu-id="3017c-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3017c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3017c-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3017c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3017c-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3017c-128">INPUTS</span></span>

## <span data-ttu-id="3017c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3017c-129">OUTPUTS</span></span>

## <span data-ttu-id="3017c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3017c-130">NOTES</span></span>

## <span data-ttu-id="3017c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3017c-131">RELATED LINKS</span></span>

