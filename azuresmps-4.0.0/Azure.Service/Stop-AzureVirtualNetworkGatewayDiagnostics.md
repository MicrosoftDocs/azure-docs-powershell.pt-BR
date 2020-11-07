---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945740"
---
# <span data-ttu-id="74174-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="74174-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="74174-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74174-102">SYNOPSIS</span></span>
<span data-ttu-id="74174-103">Interrompe uma sessão de diagnóstico do gateway de rede virtual em execução.</span><span class="sxs-lookup"><span data-stu-id="74174-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="74174-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74174-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74174-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74174-105">DESCRIPTION</span></span>
<span data-ttu-id="74174-106">O cmdlet **Stop-AzureVirtualNetworkGatewayDiagnostics** interrompe uma sessão de diagnóstico do gateway de rede virtual em execução.</span><span class="sxs-lookup"><span data-stu-id="74174-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="74174-107">Esse comando salva os resultados da sessão de diagnóstico na conta de armazenamento que o cmdlet Start-AzureVirtualNetworkGatewayDiagnostics especifica.</span><span class="sxs-lookup"><span data-stu-id="74174-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="74174-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74174-108">EXAMPLES</span></span>

## <span data-ttu-id="74174-109">OS</span><span class="sxs-lookup"><span data-stu-id="74174-109">PARAMETERS</span></span>

### <span data-ttu-id="74174-110">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="74174-110">-GatewayId</span></span>
<span data-ttu-id="74174-111">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="74174-111">Specifies the ID of a gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74174-112">-Perfil</span><span class="sxs-lookup"><span data-stu-id="74174-112">-Profile</span></span>
<span data-ttu-id="74174-113">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="74174-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="74174-114">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="74174-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74174-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74174-115">CommonParameters</span></span>
<span data-ttu-id="74174-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74174-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74174-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74174-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74174-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74174-118">INPUTS</span></span>

## <span data-ttu-id="74174-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74174-119">OUTPUTS</span></span>

## <span data-ttu-id="74174-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74174-120">NOTES</span></span>

## <span data-ttu-id="74174-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74174-121">RELATED LINKS</span></span>

[<span data-ttu-id="74174-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="74174-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="74174-123">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="74174-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


