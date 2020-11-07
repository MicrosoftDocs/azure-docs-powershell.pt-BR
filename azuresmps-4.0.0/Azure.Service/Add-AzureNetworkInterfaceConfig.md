---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FE31EE5C-830F-4B5E-82DB-C881032EF05C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c1160478da2c84f2d792ab570b05d544f4537bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946394"
---
# <span data-ttu-id="cacd1-101">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="cacd1-101">Add-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="cacd1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cacd1-102">SYNOPSIS</span></span>

## <span data-ttu-id="cacd1-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cacd1-103">SYNTAX</span></span>

```
Add-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cacd1-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cacd1-104">DESCRIPTION</span></span>

## <span data-ttu-id="cacd1-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cacd1-105">EXAMPLES</span></span>

### <span data-ttu-id="cacd1-106">1:</span><span class="sxs-lookup"><span data-stu-id="cacd1-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="cacd1-107">OS</span><span class="sxs-lookup"><span data-stu-id="cacd1-107">PARAMETERS</span></span>

### <span data-ttu-id="cacd1-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cacd1-108">-InformationAction</span></span>
<span data-ttu-id="cacd1-109">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cacd1-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cacd1-110">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cacd1-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cacd1-111">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cacd1-111">Continue</span></span>
- <span data-ttu-id="cacd1-112">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cacd1-112">Ignore</span></span>
- <span data-ttu-id="cacd1-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="cacd1-113">Inquire</span></span>
- <span data-ttu-id="cacd1-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cacd1-114">SilentlyContinue</span></span>
- <span data-ttu-id="cacd1-115">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cacd1-115">Stop</span></span>
- <span data-ttu-id="cacd1-116">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cacd1-116">Suspend</span></span>

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

### <span data-ttu-id="cacd1-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cacd1-117">-InformationVariable</span></span>
<span data-ttu-id="cacd1-118">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cacd1-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cacd1-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="cacd1-119">-IPForwarding</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacd1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cacd1-120">-Name</span></span>
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

### <span data-ttu-id="cacd1-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cacd1-121">-NetworkSecurityGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacd1-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cacd1-122">-Profile</span></span>
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

### <span data-ttu-id="cacd1-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="cacd1-123">-StaticVNetIPAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacd1-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cacd1-124">-SubnetName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cacd1-125">-VM</span><span class="sxs-lookup"><span data-stu-id="cacd1-125">-VM</span></span>
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

### <span data-ttu-id="cacd1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cacd1-126">CommonParameters</span></span>
<span data-ttu-id="cacd1-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cacd1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cacd1-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cacd1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cacd1-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cacd1-129">INPUTS</span></span>

## <span data-ttu-id="cacd1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cacd1-130">OUTPUTS</span></span>

## <span data-ttu-id="cacd1-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cacd1-131">NOTES</span></span>

## <span data-ttu-id="cacd1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cacd1-132">RELATED LINKS</span></span>

[<span data-ttu-id="cacd1-133">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="cacd1-133">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="cacd1-134">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="cacd1-134">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="cacd1-135">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="cacd1-135">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


