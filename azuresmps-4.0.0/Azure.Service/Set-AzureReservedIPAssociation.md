---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945825"
---
# <span data-ttu-id="8c327-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="8c327-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="8c327-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c327-102">SYNOPSIS</span></span>
<span data-ttu-id="8c327-103">Associa um endereço IP reservado a uma máquina virtual existente ou a um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="8c327-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="8c327-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c327-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8c327-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c327-105">DESCRIPTION</span></span>
<span data-ttu-id="8c327-106">O cmdlet **set-AzureReservedIPAssociation** associa um endereço IP reservado ao VIP (endereço IP virtual) de uma máquina virtual em execução ou serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="8c327-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="8c327-107">O endereço IP reservado não deve ser usado no momento da invocação desse cmdlet e deve estar na mesma região que a máquina virtual ou o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="8c327-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="8c327-108">A operação leva cerca de 30 segundos para ser concluída, após a qual a máquina virtual ou o serviço está acessível usando o endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="8c327-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="8c327-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c327-109">EXAMPLES</span></span>

### <span data-ttu-id="8c327-110">Exemplo 1: definir uma associação de IP reservado</span><span class="sxs-lookup"><span data-stu-id="8c327-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="8c327-111">Esse comando atribui o endereço IP reservado chamado ResIp14 ao serviço PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="8c327-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="8c327-112">ResIp14 é um IP reservado na região oeste da Europa.</span><span class="sxs-lookup"><span data-stu-id="8c327-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="8c327-113">OS</span><span class="sxs-lookup"><span data-stu-id="8c327-113">PARAMETERS</span></span>

### <span data-ttu-id="8c327-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8c327-114">-InformationAction</span></span>
<span data-ttu-id="8c327-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8c327-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8c327-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c327-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c327-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8c327-117">Continue</span></span>
- <span data-ttu-id="8c327-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8c327-118">Ignore</span></span>
- <span data-ttu-id="8c327-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="8c327-119">Inquire</span></span>
- <span data-ttu-id="8c327-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c327-120">SilentlyContinue</span></span>
- <span data-ttu-id="8c327-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8c327-121">Stop</span></span>
- <span data-ttu-id="8c327-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8c327-122">Suspend</span></span>

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

### <span data-ttu-id="8c327-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c327-123">-InformationVariable</span></span>
<span data-ttu-id="8c327-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8c327-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8c327-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8c327-125">-Profile</span></span>
<span data-ttu-id="8c327-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8c327-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c327-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8c327-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c327-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="8c327-128">-ReservedIPName</span></span>
<span data-ttu-id="8c327-129">Especifica o nome do endereço IP reservado para associar a uma máquina virtual ou a um serviço.</span><span class="sxs-lookup"><span data-stu-id="8c327-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c327-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8c327-130">-ServiceName</span></span>
<span data-ttu-id="8c327-131">Especifica o nome do serviço que tem a implantação à qual associar o endereço IP reservado.</span><span class="sxs-lookup"><span data-stu-id="8c327-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c327-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="8c327-132">-Slot</span></span>
<span data-ttu-id="8c327-133">Especifica o slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="8c327-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="8c327-134">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8c327-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8c327-135">Preparação</span><span class="sxs-lookup"><span data-stu-id="8c327-135">Staging</span></span>
- <span data-ttu-id="8c327-136">Preparo</span><span class="sxs-lookup"><span data-stu-id="8c327-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c327-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="8c327-137">-VirtualIPName</span></span>
<span data-ttu-id="8c327-138">Especifica o nome de um VIP existente para associar a um IP reservado.</span><span class="sxs-lookup"><span data-stu-id="8c327-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="8c327-139">Consulte Add-AzureVirtualIP adicionar VIPs a seu serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="8c327-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c327-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c327-140">CommonParameters</span></span>
<span data-ttu-id="8c327-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c327-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c327-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c327-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c327-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c327-143">INPUTS</span></span>

## <span data-ttu-id="8c327-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c327-144">OUTPUTS</span></span>

### <span data-ttu-id="8c327-145">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="8c327-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="8c327-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c327-146">NOTES</span></span>

## <span data-ttu-id="8c327-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c327-147">RELATED LINKS</span></span>

[<span data-ttu-id="8c327-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="8c327-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


