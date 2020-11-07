---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F34910FA-B024-4C1C-B040-671C8962C49D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 558d714c432efd1dbd8f11feb09b0bbde035e2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946288"
---
# <span data-ttu-id="77d5a-101">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="77d5a-101">Get-AzureVNetConfig</span></span>

## <span data-ttu-id="77d5a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="77d5a-103">Obtém a configuração de rede virtual do Azure da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="77d5a-103">Gets the Azure virtual network configuration from the current subscription.</span></span>

## <span data-ttu-id="77d5a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77d5a-104">SYNTAX</span></span>

```
Get-AzureVNetConfig [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="77d5a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="77d5a-106">O cmdlet **Get-AzureVNetConfig** recupera a configuração de rede virtual da assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="77d5a-106">The **Get-AzureVNetConfig** cmdlet retrieves the virtual network configuration of the current Azure subscription.</span></span>
<span data-ttu-id="77d5a-107">Se o parâmetro *ExportToFile* for especificado, um arquivo de configuração de rede será criado.</span><span class="sxs-lookup"><span data-stu-id="77d5a-107">If the *ExportToFile* parameter is specified, a network configuration file is created.</span></span>

## <span data-ttu-id="77d5a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77d5a-108">EXAMPLES</span></span>

### <span data-ttu-id="77d5a-109">Exemplo 1: obter a configuração de rede virtual de uma assinatura atual do Azure</span><span class="sxs-lookup"><span data-stu-id="77d5a-109">Example 1: Get the virtual network configuration of a current Azure subscription</span></span>
```
PS C:\> Get-AzureVNetConfig
```

<span data-ttu-id="77d5a-110">Esse comando obtém a configuração de rede virtual da assinatura atual do Azure e a exibe.</span><span class="sxs-lookup"><span data-stu-id="77d5a-110">This command gets the virtual network configuration of the current Azure subscription and displays it.</span></span>

### <span data-ttu-id="77d5a-111">Exemplo 2: obter a configuração de rede virtual da assinatura atual do Azure e salvá-la em um arquivo local</span><span class="sxs-lookup"><span data-stu-id="77d5a-111">Example 2: Get the virtual network configuration of the current Azure subscription and save it to a local file</span></span>
```
PS C:\> Get-AzureVNetConfig -ExportToFile "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="77d5a-112">Esse comando obtém a configuração de rede virtual da assinatura atual do Azure e salva-a em um arquivo local.</span><span class="sxs-lookup"><span data-stu-id="77d5a-112">This command gets the virtual network configuration of the current Azure subscription and then saves it to a local file.</span></span>

## <span data-ttu-id="77d5a-113">OS</span><span class="sxs-lookup"><span data-stu-id="77d5a-113">PARAMETERS</span></span>

### <span data-ttu-id="77d5a-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="77d5a-114">-ExportToFile</span></span>
<span data-ttu-id="77d5a-115">Especifica o caminho e o nome de um arquivo de configuração de rede a ser criado a partir das configurações.</span><span class="sxs-lookup"><span data-stu-id="77d5a-115">Specifies the path and file name of a network configuration file to be created from the settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d5a-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="77d5a-116">-InformationAction</span></span>
<span data-ttu-id="77d5a-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="77d5a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="77d5a-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="77d5a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77d5a-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="77d5a-119">Continue</span></span>
- <span data-ttu-id="77d5a-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="77d5a-120">Ignore</span></span>
- <span data-ttu-id="77d5a-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="77d5a-121">Inquire</span></span>
- <span data-ttu-id="77d5a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="77d5a-122">SilentlyContinue</span></span>
- <span data-ttu-id="77d5a-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="77d5a-123">Stop</span></span>
- <span data-ttu-id="77d5a-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="77d5a-124">Suspend</span></span>

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

### <span data-ttu-id="77d5a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="77d5a-125">-InformationVariable</span></span>
<span data-ttu-id="77d5a-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="77d5a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="77d5a-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="77d5a-127">-Profile</span></span>
<span data-ttu-id="77d5a-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="77d5a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77d5a-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="77d5a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="77d5a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d5a-130">CommonParameters</span></span>
<span data-ttu-id="77d5a-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d5a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d5a-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d5a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d5a-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77d5a-133">INPUTS</span></span>

## <span data-ttu-id="77d5a-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77d5a-134">OUTPUTS</span></span>

## <span data-ttu-id="77d5a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77d5a-135">NOTES</span></span>

## <span data-ttu-id="77d5a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77d5a-136">RELATED LINKS</span></span>

[<span data-ttu-id="77d5a-137">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="77d5a-137">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="77d5a-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="77d5a-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="77d5a-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="77d5a-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


