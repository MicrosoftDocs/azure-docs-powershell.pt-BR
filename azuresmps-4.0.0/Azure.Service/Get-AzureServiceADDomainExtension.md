---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CF429CF0-2AB2-4E31-8A0D-AE5C8D77A76B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0d1ad08d88cb5b89b0537b19f8ea4aaef0000cbb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945607"
---
# <span data-ttu-id="afa97-101">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="afa97-101">Get-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="afa97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="afa97-102">SYNOPSIS</span></span>
<span data-ttu-id="afa97-103">Obtém a extensão de domínio do serviço de nuvem do Active Directory (AD) que se aplica a todas as funções ou às funções nomeadas em um slot de implantação especificado.</span><span class="sxs-lookup"><span data-stu-id="afa97-103">Gets the cloud service Active Directory (AD) domain extension that applies to all roles or to named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="afa97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afa97-104">SYNTAX</span></span>

```
Get-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="afa97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="afa97-105">DESCRIPTION</span></span>
<span data-ttu-id="afa97-106">O cmdlet **Get-AzureServiceADDomainExtension** Obtém a extensão de domínio do AD do serviço em nuvem que se aplica a todas as funções ou funções nomeadas em um slot de implantação especificado.</span><span class="sxs-lookup"><span data-stu-id="afa97-106">The **Get-AzureServiceADDomainExtension** cmdlet gets the cloud service AD domain extension that applies to all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="afa97-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="afa97-107">EXAMPLES</span></span>

### <span data-ttu-id="afa97-108">Exemplo 1: obter a extensão de domínio do AD para um serviço especificado</span><span class="sxs-lookup"><span data-stu-id="afa97-108">Example 1: Get the AD domain extension for a specified service</span></span>
```
PS C:\> Get-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="afa97-109">Esse comando obtém a extensão de domínio do AD para o serviço especificado em $Svc.</span><span class="sxs-lookup"><span data-stu-id="afa97-109">This command gets the AD domain extension for the service specified in $Svc.</span></span>

## <span data-ttu-id="afa97-110">OS</span><span class="sxs-lookup"><span data-stu-id="afa97-110">PARAMETERS</span></span>

### <span data-ttu-id="afa97-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="afa97-111">-InformationAction</span></span>
<span data-ttu-id="afa97-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="afa97-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="afa97-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="afa97-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="afa97-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="afa97-114">Continue</span></span>
- <span data-ttu-id="afa97-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="afa97-115">Ignore</span></span>
- <span data-ttu-id="afa97-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="afa97-116">Inquire</span></span>
- <span data-ttu-id="afa97-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="afa97-117">SilentlyContinue</span></span>
- <span data-ttu-id="afa97-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="afa97-118">Stop</span></span>
- <span data-ttu-id="afa97-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="afa97-119">Suspend</span></span>

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

### <span data-ttu-id="afa97-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="afa97-120">-InformationVariable</span></span>
<span data-ttu-id="afa97-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="afa97-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="afa97-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="afa97-122">-Profile</span></span>
<span data-ttu-id="afa97-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="afa97-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="afa97-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="afa97-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="afa97-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="afa97-125">-ServiceName</span></span>
<span data-ttu-id="afa97-126">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="afa97-126">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa97-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="afa97-127">-Slot</span></span>
<span data-ttu-id="afa97-128">Especifica o ambiente de implantação.</span><span class="sxs-lookup"><span data-stu-id="afa97-128">Specifies the deployment environment.</span></span>
<span data-ttu-id="afa97-129">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="afa97-129">The acceptable values for this parameter are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa97-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa97-130">CommonParameters</span></span>
<span data-ttu-id="afa97-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afa97-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa97-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa97-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa97-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="afa97-133">INPUTS</span></span>

## <span data-ttu-id="afa97-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="afa97-134">OUTPUTS</span></span>

## <span data-ttu-id="afa97-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="afa97-135">NOTES</span></span>

## <span data-ttu-id="afa97-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="afa97-136">RELATED LINKS</span></span>

[<span data-ttu-id="afa97-137">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="afa97-137">Remove-AzureServiceADDomainExtension</span></span>](./Remove-AzureServiceADDomainExtension.md)

[<span data-ttu-id="afa97-138">Set-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="afa97-138">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


