---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945787"
---
# <span data-ttu-id="eafe1-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="eafe1-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="eafe1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eafe1-102">SYNOPSIS</span></span>
<span data-ttu-id="eafe1-103">Atualiza as configurações de rede virtual para um serviço na nuvem do Azure.</span><span class="sxs-lookup"><span data-stu-id="eafe1-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="eafe1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eafe1-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eafe1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eafe1-105">DESCRIPTION</span></span>
<span data-ttu-id="eafe1-106">O cmdlet **set-AzureVNetConfig** atualiza a configuração de rede para a assinatura atual do Azure, especificando um caminho para um arquivo de configuração de rede (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="eafe1-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="eafe1-107">O arquivo de configuração de rede define as sub-redes e os servidores DNS para serviços de nuvem em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="eafe1-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="eafe1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eafe1-108">EXAMPLES</span></span>

### <span data-ttu-id="eafe1-109">Exemplo 1: atualizar a configuração de rede da assinatura do Azure para um arquivo local</span><span class="sxs-lookup"><span data-stu-id="eafe1-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="eafe1-110">Esse comando atualiza a configuração de rede da assinatura atual do Microsoft Azure para isso no arquivo local "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="eafe1-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="eafe1-111">Exemplo 2: definir a assinatura do Azure e atualizar a configuração de rede</span><span class="sxs-lookup"><span data-stu-id="eafe1-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="eafe1-112">Este exemplo define a assinatura do Microsoft Azure e atualiza a configuração de rede dessa assinatura usando a configuração definida no arquivo local "c:\temp\MyAzNets.netcfg".</span><span class="sxs-lookup"><span data-stu-id="eafe1-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="eafe1-113">OS</span><span class="sxs-lookup"><span data-stu-id="eafe1-113">PARAMETERS</span></span>

### <span data-ttu-id="eafe1-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="eafe1-114">-ConfigurationPath</span></span>
<span data-ttu-id="eafe1-115">Especifica o caminho e o nome de arquivo de um arquivo de configuração de rede (. netcfg).</span><span class="sxs-lookup"><span data-stu-id="eafe1-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

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

### <span data-ttu-id="eafe1-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="eafe1-116">-InformationAction</span></span>
<span data-ttu-id="eafe1-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="eafe1-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eafe1-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="eafe1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eafe1-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="eafe1-119">Continue</span></span>
- <span data-ttu-id="eafe1-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="eafe1-120">Ignore</span></span>
- <span data-ttu-id="eafe1-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="eafe1-121">Inquire</span></span>
- <span data-ttu-id="eafe1-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eafe1-122">SilentlyContinue</span></span>
- <span data-ttu-id="eafe1-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="eafe1-123">Stop</span></span>
- <span data-ttu-id="eafe1-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="eafe1-124">Suspend</span></span>

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

### <span data-ttu-id="eafe1-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eafe1-125">-InformationVariable</span></span>
<span data-ttu-id="eafe1-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="eafe1-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eafe1-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="eafe1-127">-Profile</span></span>
<span data-ttu-id="eafe1-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="eafe1-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eafe1-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="eafe1-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eafe1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafe1-130">CommonParameters</span></span>
<span data-ttu-id="eafe1-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eafe1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafe1-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafe1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafe1-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eafe1-133">INPUTS</span></span>

## <span data-ttu-id="eafe1-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eafe1-134">OUTPUTS</span></span>

## <span data-ttu-id="eafe1-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eafe1-135">NOTES</span></span>

## <span data-ttu-id="eafe1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eafe1-136">RELATED LINKS</span></span>

[<span data-ttu-id="eafe1-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="eafe1-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="eafe1-138">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="eafe1-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="eafe1-139">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="eafe1-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


