---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D903741F-1D22-48FC-BFA5-6876E557EFE5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4284d34ef5151dbcd16d9ed882dcf112abbb8ea5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945492"
---
# <span data-ttu-id="fc321-101">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="fc321-101">Remove-AzureVNetConfig</span></span>

## <span data-ttu-id="fc321-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc321-102">SYNOPSIS</span></span>
<span data-ttu-id="fc321-103">Exclui a configuração de rede da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc321-103">Deletes the network configuration from the current Azure subscription.</span></span>

## <span data-ttu-id="fc321-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc321-104">SYNTAX</span></span>

```
Remove-AzureVNetConfig [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fc321-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc321-105">DESCRIPTION</span></span>
<span data-ttu-id="fc321-106">O cmdlet **Remove-AzureVNetConfig** remove todas as configurações de rede virtual da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="fc321-106">The **Remove-AzureVNetConfig** cmdlet removes all virtual network settings from the current Azure subscription.</span></span>

## <span data-ttu-id="fc321-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc321-107">EXAMPLES</span></span>

### <span data-ttu-id="fc321-108">Exemplo 1: remover uma configuração de rede virtual da assinatura atual</span><span class="sxs-lookup"><span data-stu-id="fc321-108">Example 1: Remove a virtual network configuration from the current subscription</span></span>
```
PS C:\> Remove-AzureVNetConfig
```

<span data-ttu-id="fc321-109">Este comando Remove a configuração de rede virtual da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="fc321-109">This command removes the virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="fc321-110">OS</span><span class="sxs-lookup"><span data-stu-id="fc321-110">PARAMETERS</span></span>

### <span data-ttu-id="fc321-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fc321-111">-InformationAction</span></span>
<span data-ttu-id="fc321-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="fc321-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fc321-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fc321-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc321-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="fc321-114">Continue</span></span>
- <span data-ttu-id="fc321-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="fc321-115">Ignore</span></span>
- <span data-ttu-id="fc321-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="fc321-116">Inquire</span></span>
- <span data-ttu-id="fc321-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fc321-117">SilentlyContinue</span></span>
- <span data-ttu-id="fc321-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="fc321-118">Stop</span></span>
- <span data-ttu-id="fc321-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="fc321-119">Suspend</span></span>

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

### <span data-ttu-id="fc321-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fc321-120">-InformationVariable</span></span>
<span data-ttu-id="fc321-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="fc321-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fc321-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fc321-122">-Profile</span></span>
<span data-ttu-id="fc321-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fc321-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc321-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fc321-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc321-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc321-125">CommonParameters</span></span>
<span data-ttu-id="fc321-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc321-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc321-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc321-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc321-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc321-128">INPUTS</span></span>

## <span data-ttu-id="fc321-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc321-129">OUTPUTS</span></span>

## <span data-ttu-id="fc321-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc321-130">NOTES</span></span>

## <span data-ttu-id="fc321-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc321-131">RELATED LINKS</span></span>

[<span data-ttu-id="fc321-132">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="fc321-132">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="fc321-133">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="fc321-133">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="fc321-134">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="fc321-134">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


