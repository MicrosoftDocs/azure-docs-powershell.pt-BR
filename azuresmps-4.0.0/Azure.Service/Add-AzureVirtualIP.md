---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945713"
---
# <span data-ttu-id="e6c56-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e6c56-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="e6c56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6c56-102">SYNOPSIS</span></span>
<span data-ttu-id="e6c56-103">Adiciona um IP virtual a um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="e6c56-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="e6c56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6c56-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6c56-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6c56-105">DESCRIPTION</span></span>
<span data-ttu-id="e6c56-106">O cmdlet **Add-AzureVirtualIP** adiciona um novo IP virtual (VIP) ao seu serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="e6c56-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="e6c56-107">O novo IP virtual tem um nome, mas não foi atribuído um endereço IP.</span><span class="sxs-lookup"><span data-stu-id="e6c56-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="e6c56-108">O endereço IP é alocado somente quando você associa um ponto de extremidade ao VIP.</span><span class="sxs-lookup"><span data-stu-id="e6c56-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="e6c56-109">Consulte Add-AzureEndpoint para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="e6c56-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="e6c56-110">Sua assinatura será cobrada por VIPs adicionais somente depois que elas estiverem associadas a um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="e6c56-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="e6c56-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6c56-111">EXAMPLES</span></span>

### <span data-ttu-id="e6c56-112">Exemplo 1: adicionar um IP virtual a um serviço</span><span class="sxs-lookup"><span data-stu-id="e6c56-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="e6c56-113">Esse comando adiciona um endereço IP virtual a um serviço.</span><span class="sxs-lookup"><span data-stu-id="e6c56-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="e6c56-114">OS</span><span class="sxs-lookup"><span data-stu-id="e6c56-114">PARAMETERS</span></span>

### <span data-ttu-id="e6c56-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e6c56-115">-InformationAction</span></span>
<span data-ttu-id="e6c56-116">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e6c56-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6c56-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e6c56-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6c56-118">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e6c56-118">Continue</span></span>
- <span data-ttu-id="e6c56-119">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e6c56-119">Ignore</span></span>
- <span data-ttu-id="e6c56-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="e6c56-120">Inquire</span></span>
- <span data-ttu-id="e6c56-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6c56-121">SilentlyContinue</span></span>
- <span data-ttu-id="e6c56-122">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e6c56-122">Stop</span></span>
- <span data-ttu-id="e6c56-123">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e6c56-123">Suspend</span></span>

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

### <span data-ttu-id="e6c56-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6c56-124">-InformationVariable</span></span>
<span data-ttu-id="e6c56-125">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e6c56-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e6c56-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e6c56-126">-Profile</span></span>
<span data-ttu-id="e6c56-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e6c56-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6c56-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e6c56-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6c56-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e6c56-129">-ServiceName</span></span>
<span data-ttu-id="e6c56-130">Especifica o nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="e6c56-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6c56-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="e6c56-131">-VirtualIPName</span></span>
<span data-ttu-id="e6c56-132">Especifica o nome do endereço IP virtual.</span><span class="sxs-lookup"><span data-stu-id="e6c56-132">Specifies the name of the virtual IP address.</span></span>

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

### <span data-ttu-id="e6c56-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6c56-133">CommonParameters</span></span>
<span data-ttu-id="e6c56-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6c56-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6c56-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6c56-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6c56-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6c56-136">INPUTS</span></span>

## <span data-ttu-id="e6c56-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6c56-137">OUTPUTS</span></span>

### <span data-ttu-id="e6c56-138">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="e6c56-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="e6c56-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6c56-139">NOTES</span></span>

## <span data-ttu-id="e6c56-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6c56-140">RELATED LINKS</span></span>

[<span data-ttu-id="e6c56-141">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6c56-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="e6c56-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="e6c56-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


