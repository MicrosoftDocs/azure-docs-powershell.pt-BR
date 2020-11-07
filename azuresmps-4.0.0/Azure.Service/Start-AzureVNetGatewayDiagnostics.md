---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946026"
---
# <span data-ttu-id="26f3b-101">Start-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26f3b-101">Start-AzureVNetGatewayDiagnostics</span></span>

## <span data-ttu-id="26f3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="26f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="26f3b-103">Inicia o diagnóstico do gateway para um gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="26f3b-103">Starts gateway diagnostics for a VPN gateway.</span></span>

## <span data-ttu-id="26f3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26f3b-104">SYNTAX</span></span>

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="26f3b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="26f3b-105">DESCRIPTION</span></span>
<span data-ttu-id="26f3b-106">O cmdlet **Start-AzureVNetGatewayDiagnostics** inicia uma nova sessão de diagnóstico de gateway para um gateway de rede virtual privada (VPN).</span><span class="sxs-lookup"><span data-stu-id="26f3b-106">The **Start-AzureVNetGatewayDiagnostics** cmdlet starts a new gateway diagnostics session for a virtual private network (VPN) gateway.</span></span>
<span data-ttu-id="26f3b-107">Somente uma sessão de diagnóstico do gateway pode ser executada por vez.</span><span class="sxs-lookup"><span data-stu-id="26f3b-107">Only one gateway diagnostics session can run at a time.</span></span>
<span data-ttu-id="26f3b-108">Se você executar esse cmdlet enquanto uma sessão de diagnóstico do gateway estiver em execução, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="26f3b-108">If you run this cmdlet while a gateway diagnostics session is running, this cmdlet returns an error.</span></span>

## <span data-ttu-id="26f3b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26f3b-109">EXAMPLES</span></span>

## <span data-ttu-id="26f3b-110">OS</span><span class="sxs-lookup"><span data-stu-id="26f3b-110">PARAMETERS</span></span>

### <span data-ttu-id="26f3b-111">-CaptureDurationInSeconds</span><span class="sxs-lookup"><span data-stu-id="26f3b-111">-CaptureDurationInSeconds</span></span>
<span data-ttu-id="26f3b-112">Especifica a duração da captura em segundos.</span><span class="sxs-lookup"><span data-stu-id="26f3b-112">Specifies the capture duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f3b-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="26f3b-113">-ContainerName</span></span>
<span data-ttu-id="26f3b-114">Especifica o nome de um contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="26f3b-114">Specifies the name of an Azure container.</span></span>
<span data-ttu-id="26f3b-115">Esse cmdlet armazena resultados no contêiner que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="26f3b-115">This cmdlet stores results in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="26f3b-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="26f3b-116">-Profile</span></span>
<span data-ttu-id="26f3b-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="26f3b-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="26f3b-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="26f3b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="26f3b-119">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="26f3b-119">-StorageContext</span></span>
<span data-ttu-id="26f3b-120">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="26f3b-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="26f3b-121">Esse cmdlet armazena resultados usando o contexto de armazenamento que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="26f3b-121">This cmdlet stores results by using the storage context that this parameter specifies.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f3b-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="26f3b-122">-VNetName</span></span>
<span data-ttu-id="26f3b-123">Especifica a rede virtual que contém um gateway de rede virtual para o qual esse cmdlet executa diagnósticos.</span><span class="sxs-lookup"><span data-stu-id="26f3b-123">Specifies the virtual network that contains a virtual network gateway for which this cmdlet runs diagnostics.</span></span>

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

### <span data-ttu-id="26f3b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f3b-124">CommonParameters</span></span>
<span data-ttu-id="26f3b-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26f3b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f3b-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26f3b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f3b-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="26f3b-127">INPUTS</span></span>

## <span data-ttu-id="26f3b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="26f3b-128">OUTPUTS</span></span>

## <span data-ttu-id="26f3b-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="26f3b-129">NOTES</span></span>

## <span data-ttu-id="26f3b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26f3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="26f3b-131">Get-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26f3b-131">Get-AzureVNetGatewayDiagnostics</span></span>](./Get-AzureVNetGatewayDiagnostics.md)

[<span data-ttu-id="26f3b-132">Parar-AzureVNetGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="26f3b-132">Stop-AzureVNetGatewayDiagnostics</span></span>](./Stop-AzureVNetGatewayDiagnostics.md)


