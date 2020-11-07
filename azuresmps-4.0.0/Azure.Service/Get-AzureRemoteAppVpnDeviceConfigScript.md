---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945625"
---
# <span data-ttu-id="a56c6-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="a56c6-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="a56c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a56c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a56c6-103">Recupera o script de configuração de um dispositivo VPN do RemoteApp do Azure.</span><span class="sxs-lookup"><span data-stu-id="a56c6-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="a56c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a56c6-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a56c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a56c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a56c6-106">O cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** recupera o script de configuração para um dispositivo de rede virtual privada (VPN) do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a56c6-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="a56c6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a56c6-107">EXAMPLES</span></span>

### <span data-ttu-id="a56c6-108">Exemplo 1: obter um script de configuração para um dispositivo VPN</span><span class="sxs-lookup"><span data-stu-id="a56c6-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="a56c6-109">Esse comando retorna o arquivo de script ou configuração usado para configurar o dispositivo VPN para a rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="a56c6-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="a56c6-110">Este arquivo de configuração ou script deve ser executado ou carregado no dispositivo VPN da maneira habitual para esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a56c6-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="a56c6-111">Consulte o fornecedor do dispositivo VPN para obter os requisitos exclusivos de cada dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a56c6-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="a56c6-112">OS</span><span class="sxs-lookup"><span data-stu-id="a56c6-112">PARAMETERS</span></span>

### <span data-ttu-id="a56c6-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="a56c6-113">-OSFamily</span></span>
<span data-ttu-id="a56c6-114">Especifica a família do sistema operacional (SO) que é executada na plataforma do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a56c6-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a56c6-115">-Plataforma</span><span class="sxs-lookup"><span data-stu-id="a56c6-115">-Platform</span></span>
<span data-ttu-id="a56c6-116">Especifica a plataforma do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a56c6-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a56c6-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a56c6-117">-Profile</span></span>
<span data-ttu-id="a56c6-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a56c6-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a56c6-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a56c6-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a56c6-120">-Fornecedor</span><span class="sxs-lookup"><span data-stu-id="a56c6-120">-Vendor</span></span>
<span data-ttu-id="a56c6-121">Especifica o fornecedor do dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="a56c6-121">Specifies the vendor of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a56c6-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a56c6-122">-VNetName</span></span>
<span data-ttu-id="a56c6-123">Especifica o nome de uma rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="a56c6-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a56c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a56c6-124">CommonParameters</span></span>
<span data-ttu-id="a56c6-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a56c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a56c6-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a56c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a56c6-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a56c6-127">INPUTS</span></span>

## <span data-ttu-id="a56c6-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a56c6-128">OUTPUTS</span></span>

## <span data-ttu-id="a56c6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a56c6-129">NOTES</span></span>

## <span data-ttu-id="a56c6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a56c6-130">RELATED LINKS</span></span>

[<span data-ttu-id="a56c6-131">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="a56c6-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


