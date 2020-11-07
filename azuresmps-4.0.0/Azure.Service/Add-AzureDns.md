---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AF4DF7EC-95BA-44E2-AB9B-5C8FE45CCE4C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83c0858d813c157301098f680fa9d2a90ef6950a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945734"
---
# <span data-ttu-id="6e541-101">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6e541-101">Add-AzureDns</span></span>

## <span data-ttu-id="6e541-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6e541-102">SYNOPSIS</span></span>
<span data-ttu-id="6e541-103">Adiciona um servidor DNS a um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e541-103">Adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="6e541-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e541-104">SYNTAX</span></span>

```
Add-AzureDns [-Name] <String> [-IPAddress] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6e541-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6e541-105">DESCRIPTION</span></span>
<span data-ttu-id="6e541-106">O cmdlet **Add-AzureDns** adiciona um servidor DNS a um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e541-106">The **Add-AzureDns** cmdlet adds a DNS server to an Azure service.</span></span>

## <span data-ttu-id="6e541-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e541-107">EXAMPLES</span></span>

### <span data-ttu-id="6e541-108">Exemplo 1: adicionar um servidor DNS</span><span class="sxs-lookup"><span data-stu-id="6e541-108">Example 1: Add a DNS server</span></span>
```
PS C:\> Add-AzureDns -ServiceName "ContosoService" -IPAddress 10.1.2.4 -Name "Dns07"
```

<span data-ttu-id="6e541-109">Esse comando adiciona o servidor DNS que tem o endereço 10.1.2.4 ao ContosoService.</span><span class="sxs-lookup"><span data-stu-id="6e541-109">This command adds the DNS server that has the address 10.1.2.4 to ContosoService.</span></span>

## <span data-ttu-id="6e541-110">OS</span><span class="sxs-lookup"><span data-stu-id="6e541-110">PARAMETERS</span></span>

### <span data-ttu-id="6e541-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="6e541-111">-InformationAction</span></span>
<span data-ttu-id="6e541-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="6e541-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6e541-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="6e541-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6e541-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="6e541-114">Continue</span></span>
- <span data-ttu-id="6e541-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="6e541-115">Ignore</span></span>
- <span data-ttu-id="6e541-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="6e541-116">Inquire</span></span>
- <span data-ttu-id="6e541-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6e541-117">SilentlyContinue</span></span>
- <span data-ttu-id="6e541-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="6e541-118">Stop</span></span>
- <span data-ttu-id="6e541-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="6e541-119">Suspend</span></span>

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

### <span data-ttu-id="6e541-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6e541-120">-InformationVariable</span></span>
<span data-ttu-id="6e541-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="6e541-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="6e541-122">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="6e541-122">-IPAddress</span></span>
<span data-ttu-id="6e541-123">Especifica o endereço IP do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="6e541-123">Specifies the IP address of the DNS server.</span></span>

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

### <span data-ttu-id="6e541-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e541-124">-Name</span></span>
<span data-ttu-id="6e541-125">Especifica um nome amigável para o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="6e541-125">Specifies a friendly name for the DNS server.</span></span>
<span data-ttu-id="6e541-126">Esse nome não é necessariamente um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="6e541-126">This name is not necessarily a fully qualified domain name.</span></span>

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

### <span data-ttu-id="6e541-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6e541-127">-Profile</span></span>
<span data-ttu-id="6e541-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6e541-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6e541-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6e541-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6e541-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6e541-130">-ServiceName</span></span>
<span data-ttu-id="6e541-131">Especifica o nome do serviço para o qual esse cmdlet adiciona o servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="6e541-131">Specifies the name of the service to which this cmdlet adds the DNS server.</span></span>

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

### <span data-ttu-id="6e541-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e541-132">CommonParameters</span></span>
<span data-ttu-id="6e541-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e541-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e541-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e541-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e541-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6e541-135">INPUTS</span></span>

## <span data-ttu-id="6e541-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6e541-136">OUTPUTS</span></span>

### <span data-ttu-id="6e541-137">Microsoft. WindowsAzure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="6e541-137">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="6e541-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6e541-138">NOTES</span></span>

## <span data-ttu-id="6e541-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e541-139">RELATED LINKS</span></span>

[<span data-ttu-id="6e541-140">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6e541-140">Get-AzureDns</span></span>](./Get-AzureDns.md)

[<span data-ttu-id="6e541-141">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6e541-141">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="6e541-142">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6e541-142">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="6e541-143">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="6e541-143">Set-AzureDns</span></span>](./Set-AzureDns.md)


