---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A4E88106-1B47-4ACD-8F35-027D16EA7791
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b3422581fa884245807f258adcc31d52404c53
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945805"
---
# <span data-ttu-id="bf49b-101">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bf49b-101">Set-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="bf49b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf49b-102">SYNOPSIS</span></span>

## <span data-ttu-id="bf49b-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf49b-103">SYNTAX</span></span>

```
Set-AzureNetworkInterfaceConfig [-Name] <String> [-SubnetName] <String> [[-StaticVNetIPAddress] <String>]
 [[-NetworkSecurityGroup] <String>] [[-IPForwarding] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf49b-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf49b-104">DESCRIPTION</span></span>

## <span data-ttu-id="bf49b-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf49b-105">EXAMPLES</span></span>

### <span data-ttu-id="bf49b-106">1:</span><span class="sxs-lookup"><span data-stu-id="bf49b-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="bf49b-107">OS</span><span class="sxs-lookup"><span data-stu-id="bf49b-107">PARAMETERS</span></span>

### <span data-ttu-id="bf49b-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bf49b-108">-InformationAction</span></span>
<span data-ttu-id="bf49b-109">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bf49b-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf49b-110">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bf49b-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf49b-111">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bf49b-111">Continue</span></span>
- <span data-ttu-id="bf49b-112">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bf49b-112">Ignore</span></span>
- <span data-ttu-id="bf49b-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="bf49b-113">Inquire</span></span>
- <span data-ttu-id="bf49b-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf49b-114">SilentlyContinue</span></span>
- <span data-ttu-id="bf49b-115">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bf49b-115">Stop</span></span>
- <span data-ttu-id="bf49b-116">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bf49b-116">Suspend</span></span>

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

### <span data-ttu-id="bf49b-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf49b-117">-InformationVariable</span></span>
<span data-ttu-id="bf49b-118">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bf49b-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf49b-119">-IPForwarding</span><span class="sxs-lookup"><span data-stu-id="bf49b-119">-IPForwarding</span></span>
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

### <span data-ttu-id="bf49b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf49b-120">-Name</span></span>
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

### <span data-ttu-id="bf49b-121">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bf49b-121">-NetworkSecurityGroup</span></span>
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

### <span data-ttu-id="bf49b-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bf49b-122">-Profile</span></span>
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

### <span data-ttu-id="bf49b-123">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="bf49b-123">-StaticVNetIPAddress</span></span>
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

### <span data-ttu-id="bf49b-124">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bf49b-124">-SubnetName</span></span>
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

### <span data-ttu-id="bf49b-125">-VM</span><span class="sxs-lookup"><span data-stu-id="bf49b-125">-VM</span></span>
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

### <span data-ttu-id="bf49b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf49b-126">CommonParameters</span></span>
<span data-ttu-id="bf49b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf49b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf49b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf49b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf49b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf49b-129">INPUTS</span></span>

## <span data-ttu-id="bf49b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf49b-130">OUTPUTS</span></span>

## <span data-ttu-id="bf49b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf49b-131">NOTES</span></span>

## <span data-ttu-id="bf49b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf49b-132">RELATED LINKS</span></span>

[<span data-ttu-id="bf49b-133">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bf49b-133">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="bf49b-134">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bf49b-134">Get-AzureNetworkInterfaceConfig</span></span>](./Get-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="bf49b-135">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="bf49b-135">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)


