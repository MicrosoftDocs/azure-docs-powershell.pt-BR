---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946019"
---
# <span data-ttu-id="4bfbd-101">Stop-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4bfbd-101">Stop-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="4bfbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4bfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfbd-103">Interrompe uma sessão de diagnóstico do gateway VPN em execução.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-103">Stops a running VPN gateway diagnostics session.</span></span>

## <span data-ttu-id="4bfbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bfbd-104">SYNTAX</span></span>

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4bfbd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4bfbd-105">DESCRIPTION</span></span>
<span data-ttu-id="4bfbd-106">O cmdlet **Stop-AzureVNetGatewayDiagnostics** interrompe uma sessão de diagnóstico de gateway de rede privada virtual (VPN) em execução.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-106">The **Stop-AzureVNetGatewayDiagnostics** cmdlet stops a running virtual private network (VPN) gateway diagnostics session.</span></span>
<span data-ttu-id="4bfbd-107">Esse comando salva os resultados da sessão de diagnóstico na conta de armazenamento que o cmdlet **Start-AzureVNetGatewayDiagnostics** especifica.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-107">This command saves the results of the diagnostics session to the storage account that the **Start-AzureVNetGatewayDiagnostics** cmdlet specifies.</span></span>

## <span data-ttu-id="4bfbd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bfbd-108">EXAMPLES</span></span>

## <span data-ttu-id="4bfbd-109">OS</span><span class="sxs-lookup"><span data-stu-id="4bfbd-109">PARAMETERS</span></span>

### <span data-ttu-id="4bfbd-110">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4bfbd-110">-Profile</span></span>
<span data-ttu-id="4bfbd-111">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="4bfbd-112">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4bfbd-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="4bfbd-113">-VNetName</span></span>
<span data-ttu-id="4bfbd-114">Especifica a rede virtual que contém um gateway de rede virtual para o qual esse cmdlet interrompe o diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet stops diagnostics.</span></span>

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

### <span data-ttu-id="4bfbd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfbd-115">CommonParameters</span></span>
<span data-ttu-id="4bfbd-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bfbd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfbd-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bfbd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfbd-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4bfbd-118">INPUTS</span></span>

## <span data-ttu-id="4bfbd-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4bfbd-119">OUTPUTS</span></span>

## <span data-ttu-id="4bfbd-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4bfbd-120">NOTES</span></span>

## <span data-ttu-id="4bfbd-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bfbd-121">RELATED LINKS</span></span>

[<span data-ttu-id="4bfbd-122">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4bfbd-122">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="4bfbd-123">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="4bfbd-123">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)


