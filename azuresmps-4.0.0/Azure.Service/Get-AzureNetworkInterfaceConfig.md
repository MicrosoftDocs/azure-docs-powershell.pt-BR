---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EE96AC92-02A8-4A40-A26D-0882673E51A5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2dca85290564217f5c4c319ef3531d4c31500fcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946584"
---
# <span data-ttu-id="7825d-101">Get-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="7825d-101">Get-AzureNetworkInterfaceConfig</span></span>

## <span data-ttu-id="7825d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7825d-102">SYNOPSIS</span></span>

## <span data-ttu-id="7825d-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7825d-103">SYNTAX</span></span>

```
Get-AzureNetworkInterfaceConfig [[-Name] <String>] -VM <PersistentVMRoleContext>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7825d-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7825d-104">DESCRIPTION</span></span>

## <span data-ttu-id="7825d-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7825d-105">EXAMPLES</span></span>

### <span data-ttu-id="7825d-106">1:</span><span class="sxs-lookup"><span data-stu-id="7825d-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="7825d-107">OS</span><span class="sxs-lookup"><span data-stu-id="7825d-107">PARAMETERS</span></span>

### <span data-ttu-id="7825d-108">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7825d-108">-InformationAction</span></span>
<span data-ttu-id="7825d-109">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="7825d-109">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7825d-110">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7825d-110">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7825d-111">Contínuo</span><span class="sxs-lookup"><span data-stu-id="7825d-111">Continue</span></span>
- <span data-ttu-id="7825d-112">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7825d-112">Ignore</span></span>
- <span data-ttu-id="7825d-113">Inquire</span><span class="sxs-lookup"><span data-stu-id="7825d-113">Inquire</span></span>
- <span data-ttu-id="7825d-114">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7825d-114">SilentlyContinue</span></span>
- <span data-ttu-id="7825d-115">Finaliza</span><span class="sxs-lookup"><span data-stu-id="7825d-115">Stop</span></span>
- <span data-ttu-id="7825d-116">Suspensão</span><span class="sxs-lookup"><span data-stu-id="7825d-116">Suspend</span></span>

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

### <span data-ttu-id="7825d-117">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7825d-117">-InformationVariable</span></span>
<span data-ttu-id="7825d-118">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="7825d-118">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7825d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7825d-119">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7825d-120">-VM</span><span class="sxs-lookup"><span data-stu-id="7825d-120">-VM</span></span>
```yaml
Type: PersistentVMRoleContext
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7825d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7825d-121">CommonParameters</span></span>
<span data-ttu-id="7825d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7825d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7825d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7825d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7825d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7825d-124">INPUTS</span></span>

## <span data-ttu-id="7825d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7825d-125">OUTPUTS</span></span>

## <span data-ttu-id="7825d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7825d-126">NOTES</span></span>

## <span data-ttu-id="7825d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7825d-127">RELATED LINKS</span></span>

[<span data-ttu-id="7825d-128">Add-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="7825d-128">Add-AzureNetworkInterfaceConfig</span></span>](./Add-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="7825d-129">Remove-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="7825d-129">Remove-AzureNetworkInterfaceConfig</span></span>](./Remove-AzureNetworkInterfaceConfig.md)

[<span data-ttu-id="7825d-130">Set-AzureNetworkInterfaceConfig</span><span class="sxs-lookup"><span data-stu-id="7825d-130">Set-AzureNetworkInterfaceConfig</span></span>](./Set-AzureNetworkInterfaceConfig.md)


