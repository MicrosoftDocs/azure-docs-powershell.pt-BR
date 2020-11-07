---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: DA5689DF-AA4A-4161-89B0-8055BF384274
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b71367ac18a753fad5425d0073b55cacb413e4b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945772"
---
# <span data-ttu-id="31971-101">Start-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="31971-101">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="31971-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31971-102">SYNOPSIS</span></span>
<span data-ttu-id="31971-103">Inicia o diagnóstico para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="31971-103">Starts diagnostics for a virtual network gateway.</span></span>

## <span data-ttu-id="31971-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31971-104">SYNTAX</span></span>

```
Start-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-CaptureDurationInSeconds <Int32>]
 [-ContainerName <String>] [-StorageContext <AzureStorageContext>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="31971-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31971-105">DESCRIPTION</span></span>
<span data-ttu-id="31971-106">O cmdlet **Start-AzureVirtualNetworkGatewayDiagnostics** inicia uma nova sessão de diagnóstico de gateway para um gateway de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="31971-106">The **Start-AzureVirtualNetworkGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual network gateway.</span></span>
<span data-ttu-id="31971-107">Somente uma sessão de diagnóstico do gateway pode ser executada por vez.</span><span class="sxs-lookup"><span data-stu-id="31971-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="31971-108">Se você executar esse cmdlet enquanto uma sessão de diagnóstico do gateway estiver em execução, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="31971-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="31971-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31971-109">EXAMPLES</span></span>

## <span data-ttu-id="31971-110">OS</span><span class="sxs-lookup"><span data-stu-id="31971-110">PARAMETERS</span></span>

### <span data-ttu-id="31971-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="31971-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="31971-112">Especifica a duração da captura em segundos.</span><span class="sxs-lookup"><span data-stu-id="31971-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31971-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="31971-113">-ContainerName</span></span>
<span data-ttu-id="31971-114">Especifica o nome de um contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="31971-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="31971-115">Esse cmdlet armazena resultados no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="31971-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="31971-116">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="31971-116">-GatewayId</span></span>
<span data-ttu-id="31971-117">Especifica a ID de um gateway.</span><span class="sxs-lookup"><span data-stu-id="31971-117">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="31971-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="31971-118">-Profile</span></span>
<span data-ttu-id="31971-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="31971-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="31971-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="31971-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31971-121">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="31971-121">-StorageContext</span></span>
<span data-ttu-id="31971-122">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="31971-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="31971-123">Esse cmdlet armazena resultados usando o contexto de armazenamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="31971-123">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31971-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31971-124">CommonParameters</span></span>
<span data-ttu-id="31971-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31971-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31971-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31971-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31971-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31971-127">INPUTS</span></span>

## <span data-ttu-id="31971-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31971-128">OUTPUTS</span></span>

## <span data-ttu-id="31971-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31971-129">NOTES</span></span>

## <span data-ttu-id="31971-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31971-130">RELATED LINKS</span></span>

[<span data-ttu-id="31971-131">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="31971-131">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="31971-132">Parar-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="31971-132">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


