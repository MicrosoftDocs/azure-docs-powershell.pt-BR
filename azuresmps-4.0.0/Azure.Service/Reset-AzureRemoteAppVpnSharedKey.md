---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945471"
---
# <span data-ttu-id="b2e08-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="b2e08-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="b2e08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2e08-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e08-103">Redefine a chave compartilhada da VPN do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b2e08-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="b2e08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2e08-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b2e08-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2e08-105">DESCRIPTION</span></span>
<span data-ttu-id="b2e08-106">O cmdlet **Reset-AzureRemoteAppVpnSharedKey** redefine a chave compartilhada da rede virtual privada (VPN) do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b2e08-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="b2e08-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2e08-107">EXAMPLES</span></span>

### <span data-ttu-id="b2e08-108">Exemplo 1: redefinir a chave compartilhada em uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="b2e08-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="b2e08-109">Esse comando redefine a chave compartilhada na rede virtual chamada ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="b2e08-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="b2e08-110">A conexão VPN com a rede local permanecerá offline até que a nova chave compartilhada seja configurada no dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b2e08-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="b2e08-111">Para configurar o dispositivo VPN, use o cmdlet **Get-AzureRemoteAppVpnDeviceConfigScript** para recuperar o arquivo de configuração ou o script correto para o seu dispositivo VPN e, em seguida, carregue o arquivo de configuração ou o script no dispositivo VPN.</span><span class="sxs-lookup"><span data-stu-id="b2e08-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="b2e08-112">OS</span><span class="sxs-lookup"><span data-stu-id="b2e08-112">PARAMETERS</span></span>

### <span data-ttu-id="b2e08-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b2e08-113">-Profile</span></span>
<span data-ttu-id="b2e08-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b2e08-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b2e08-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b2e08-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b2e08-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b2e08-116">-VNetName</span></span>
<span data-ttu-id="b2e08-117">Especifica o nome da rede virtual do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b2e08-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="b2e08-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2e08-118">-Confirm</span></span>
<span data-ttu-id="b2e08-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2e08-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e08-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2e08-120">-WhatIf</span></span>
<span data-ttu-id="b2e08-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2e08-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2e08-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2e08-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e08-123">CommonParameters</span></span>
<span data-ttu-id="b2e08-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e08-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2e08-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e08-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2e08-126">INPUTS</span></span>

## <span data-ttu-id="b2e08-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2e08-127">OUTPUTS</span></span>

### <span data-ttu-id="b2e08-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b2e08-128">System.String</span></span>

## <span data-ttu-id="b2e08-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2e08-129">NOTES</span></span>

## <span data-ttu-id="b2e08-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2e08-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2e08-131">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="b2e08-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="b2e08-132">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="b2e08-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


