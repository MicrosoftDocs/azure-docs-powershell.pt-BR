---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945646"
---
# <span data-ttu-id="e9927-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e9927-101">Get-AzureDns</span></span>

## <span data-ttu-id="e9927-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9927-102">SYNOPSIS</span></span>
<span data-ttu-id="e9927-103">Obtém as configurações de DNS para uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9927-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="e9927-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9927-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e9927-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9927-105">DESCRIPTION</span></span>
<span data-ttu-id="e9927-106">O cmdlet **Get-AzureDns** Obtém as configurações de DNS para uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9927-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="e9927-107">O cmdlet retorna o nome amigável e o endereço IP do servidor DNS em um objeto de configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="e9927-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="e9927-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9927-108">EXAMPLES</span></span>

### <span data-ttu-id="e9927-109">Exemplo 1: obter configurações de DNS</span><span class="sxs-lookup"><span data-stu-id="e9927-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="e9927-110">Esse comando usa o cmdlet **Get-AzureDeployment** para obter a implantação de produção do serviço chamado ContosoService.</span><span class="sxs-lookup"><span data-stu-id="e9927-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="e9927-111">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="e9927-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e9927-112">O cmdlet atual Obtém as configurações de DNS.</span><span class="sxs-lookup"><span data-stu-id="e9927-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="e9927-113">OS</span><span class="sxs-lookup"><span data-stu-id="e9927-113">PARAMETERS</span></span>

### <span data-ttu-id="e9927-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="e9927-114">-DnsSettings</span></span>
<span data-ttu-id="e9927-115">Especifica um objeto **DnsSettings** .</span><span class="sxs-lookup"><span data-stu-id="e9927-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9927-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e9927-116">-InformationAction</span></span>
<span data-ttu-id="e9927-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e9927-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e9927-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e9927-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e9927-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e9927-119">Continue</span></span>
- <span data-ttu-id="e9927-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e9927-120">Ignore</span></span>
- <span data-ttu-id="e9927-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="e9927-121">Inquire</span></span>
- <span data-ttu-id="e9927-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e9927-122">SilentlyContinue</span></span>
- <span data-ttu-id="e9927-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e9927-123">Stop</span></span>
- <span data-ttu-id="e9927-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e9927-124">Suspend</span></span>

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

### <span data-ttu-id="e9927-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e9927-125">-InformationVariable</span></span>
<span data-ttu-id="e9927-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e9927-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e9927-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9927-127">CommonParameters</span></span>
<span data-ttu-id="e9927-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9927-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9927-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9927-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9927-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9927-130">INPUTS</span></span>

## <span data-ttu-id="e9927-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9927-131">OUTPUTS</span></span>

## <span data-ttu-id="e9927-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9927-132">NOTES</span></span>

## <span data-ttu-id="e9927-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9927-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9927-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e9927-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="e9927-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="e9927-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="e9927-136">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e9927-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="e9927-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e9927-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="e9927-138">Set-AzureDns</span><span class="sxs-lookup"><span data-stu-id="e9927-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


