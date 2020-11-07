---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 185C2680-501F-497D-81B2-5F6E30A91F16
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55e9f6f026e7e524613a0e070767bc2ab26f6d66
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946466"
---
# <span data-ttu-id="339aa-101">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="339aa-101">Remove-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="339aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="339aa-102">SYNOPSIS</span></span>

## <span data-ttu-id="339aa-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="339aa-103">SYNTAX</span></span>

```
Remove-AzureNetworkInterfaceConfig [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="339aa-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="339aa-104">DESCRIPTION</span></span>

## <span data-ttu-id="339aa-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="339aa-105">EXAMPLES</span></span>

### <span data-ttu-id="339aa-106">1:</span><span class="sxs-lookup"><span data-stu-id="339aa-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="339aa-107">OS</span><span class="sxs-lookup"><span data-stu-id="339aa-107">PARAMETERS</span></span>

### <span data-ttu-id="339aa-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="339aa-108">-InformationAction</span></span>
<span data-ttu-id="339aa-109">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="339aa-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="339aa-110">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="339aa-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="339aa-111">Contínuo</span><span class="sxs-lookup"><span data-stu-id="339aa-111">Continue</span></span>
- <span data-ttu-id="339aa-112">Ignorar</span><span class="sxs-lookup"><span data-stu-id="339aa-112">Ignore</span></span>
- <span data-ttu-id="339aa-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="339aa-113">Inquire</span></span>
- <span data-ttu-id="339aa-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="339aa-114">SilentlyContinue</span></span>
- <span data-ttu-id="339aa-115">Finaliza</span><span class="sxs-lookup"><span data-stu-id="339aa-115">Stop</span></span>
- <span data-ttu-id="339aa-116">Suspensão</span><span class="sxs-lookup"><span data-stu-id="339aa-116">Suspend</span></span>

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

### <span data-ttu-id="339aa-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="339aa-117">-InformationVariable</span></span>
<span data-ttu-id="339aa-118">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="339aa-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="339aa-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="339aa-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="339aa-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="339aa-120">-Profile</span></span>
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

### <span data-ttu-id="339aa-121">-VM</span><span class="sxs-lookup"><span data-stu-id="339aa-121">-VM</span></span>
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

### <span data-ttu-id="339aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339aa-122">CommonParameters</span></span>
<span data-ttu-id="339aa-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339aa-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339aa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339aa-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="339aa-125">INPUTS</span></span>

## <span data-ttu-id="339aa-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="339aa-126">OUTPUTS</span></span>

## <span data-ttu-id="339aa-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="339aa-127">NOTES</span></span>

## <span data-ttu-id="339aa-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="339aa-128">RELATED LINKS</span></span>

[<span data-ttu-id="339aa-129">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="339aa-129">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="339aa-130">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="339aa-130">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="339aa-131">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="339aa-131">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


