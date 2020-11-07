---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5BC16303-CCB4-40D8-ABCB-59CF0D85ED63
online version: ''
schema: 2.0.0
ms.openlocfilehash: f24f5d8f7f72c59847cfa5dde51a1937bc304735
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946069"
---
# <span data-ttu-id="887d8-101">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="887d8-101">Set-AzureDns</span></span>

## <span data-ttu-id="887d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="887d8-102">SYNOPSIS</span></span>
<span data-ttu-id="887d8-103">Modifica o endereço IP de um servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="887d8-103">Modifies the IP address of a DNS server.</span></span>

## <span data-ttu-id="887d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="887d8-104">SYNTAX</span></span>

```
Set-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="887d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="887d8-105">DESCRIPTION</span></span>
<span data-ttu-id="887d8-106">O cmdlet **set-AzureDns** modifica o endereço IP de um servidor DNS para um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="887d8-106">The **Set-AzureDns** cmdlet modifies the IP address of a DNS server for an Azure service.</span></span>

## <span data-ttu-id="887d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="887d8-107">EXAMPLES</span></span>

### <span data-ttu-id="887d8-108">Exemplo 1: modificar o endereço IP de um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="887d8-108">Example 1: Modify the IP address of a DNS server</span></span>
```
PS C:\> Set-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.5 -Name "Dns07"
```

<span data-ttu-id="887d8-109">Esse comando modifica o endereço IP do servidor DNS chamado Dns07 para o serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="887d8-109">This command modifies the IP address of the DNS server named Dns07 for the service named ContosoService.</span></span>

## <span data-ttu-id="887d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="887d8-110">PARAMETERS</span></span>

### <span data-ttu-id="887d8-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="887d8-111">-InformationAction</span></span>
<span data-ttu-id="887d8-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="887d8-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="887d8-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="887d8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="887d8-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="887d8-114">Continue</span></span>
- <span data-ttu-id="887d8-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="887d8-115">Ignore</span></span>
- <span data-ttu-id="887d8-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="887d8-116">Inquire</span></span>
- <span data-ttu-id="887d8-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="887d8-117">SilentlyContinue</span></span>
- <span data-ttu-id="887d8-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="887d8-118">Stop</span></span>
- <span data-ttu-id="887d8-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="887d8-119">Suspend</span></span>

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

### <span data-ttu-id="887d8-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="887d8-120">-InformationVariable</span></span>
<span data-ttu-id="887d8-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="887d8-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="887d8-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="887d8-122">-IPAddress</span></span>
<span data-ttu-id="887d8-123">Especifica o novo endereço IP do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="887d8-123">Specifies the new IP address of the DNS server.</span></span>

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

### <span data-ttu-id="887d8-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="887d8-124">-Name</span></span>
<span data-ttu-id="887d8-125">Especifica o nome do servidor DNS que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="887d8-125">Specifies the name of the DNS server that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="887d8-126">-Perfil</span><span class="sxs-lookup"><span data-stu-id="887d8-126">-Profile</span></span>
<span data-ttu-id="887d8-127">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="887d8-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="887d8-128">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="887d8-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="887d8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="887d8-129">-ServiceName</span></span>
<span data-ttu-id="887d8-130">Especifica o nome do serviço para o qual esse cmdlet modifica o endereço do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="887d8-130">Specifies the name of the service for which this cmdlet modifies the address of the DNS server.</span></span>

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

### <span data-ttu-id="887d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887d8-131">CommonParameters</span></span>
<span data-ttu-id="887d8-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887d8-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="887d8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887d8-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="887d8-134">INPUTS</span></span>

## <span data-ttu-id="887d8-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="887d8-135">OUTPUTS</span></span>

### <span data-ttu-id="887d8-136">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="887d8-136">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="887d8-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="887d8-137">NOTES</span></span>

## <span data-ttu-id="887d8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="887d8-138">RELATED LINKS</span></span>

[<span data-ttu-id="887d8-139">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="887d8-139">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="887d8-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="887d8-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="887d8-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="887d8-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="887d8-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="887d8-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)


