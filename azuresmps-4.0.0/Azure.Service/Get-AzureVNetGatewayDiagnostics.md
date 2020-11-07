---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946277"
---
# <span data-ttu-id="828e8-101">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="828e8-101">Get-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="828e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="828e8-102">SYNOPSIS</span></span>
<span data-ttu-id="828e8-103">Obtém o estado atual do diagnóstico para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="828e8-103">Gets the current state of diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="828e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="828e8-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="828e8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="828e8-105">DESCRIPTION</span></span>
<span data-ttu-id="828e8-106">O cmdlet **Get-AzureVNetGatewayDiagnostics** Obtém o estado atual do diagnóstico para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="828e8-106">The **Get-AzureVNetGatewayDiagnostics** cmdlet gets the current state of diagnostics for a virtual network gateway.</span></span>
<span data-ttu-id="828e8-107">Se um objeto Binary Large (BLOB) existir em que o **Start-AzureVNetGatewayDiagnostics** salvou uma sessão de diagnóstico anterior, esse cmdlet também retornará a URL do blob em que esse cmdlet salvou essa sessão de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="828e8-107">If a binary large object (blob) exists where the **Start-AzureVNetGatewayDiagnostics** saved a previous diagnostics session, this cmdlet also returns the URL of the blob where that cmdlet saved that diagnostics session.</span></span>

## <span data-ttu-id="828e8-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="828e8-108">EXAMPLES</span></span>

## <span data-ttu-id="828e8-109">OS</span><span class="sxs-lookup"><span data-stu-id="828e8-109">PARAMETERS</span></span>

### <span data-ttu-id="828e8-110">-Perfil</span><span class="sxs-lookup"><span data-stu-id="828e8-110">-Profile</span></span>
<span data-ttu-id="828e8-111">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="828e8-111">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="828e8-112">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="828e8-112">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="828e8-113">-VNetName</span><span class="sxs-lookup"><span data-stu-id="828e8-113">-VNetName</span></span>
<span data-ttu-id="828e8-114">Especifica a rede virtual que contém um gateway de rede virtual para o qual esse cmdlet obtém diagnósticos.</span><span class="sxs-lookup"><span data-stu-id="828e8-114">Specifies the virtual network that contains a virtual network gateway for which this cmdlet gets diagnostics.</span></span>

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

### <span data-ttu-id="828e8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828e8-115">CommonParameters</span></span>
<span data-ttu-id="828e8-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828e8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828e8-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828e8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828e8-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="828e8-118">INPUTS</span></span>

## <span data-ttu-id="828e8-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="828e8-119">OUTPUTS</span></span>

## <span data-ttu-id="828e8-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="828e8-120">NOTES</span></span>

## <span data-ttu-id="828e8-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="828e8-121">RELATED LINKS</span></span>

[<span data-ttu-id="828e8-122">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="828e8-122">Start-AzureVNetGatewayDiagnostics</span></span>](./Start-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="828e8-123">Parar-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="828e8-123">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


