---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BED3D3FE-D1E8-4857-A675-7B2670A129B2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 039afbea4d4eb6736cf3b0faebf189edef2d9c26
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946226"
---
# <span data-ttu-id="7943d-101">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-101">New-AzureApplicationGateway</span></span>

## <span data-ttu-id="7943d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7943d-102">SYNOPSIS</span></span>
<span data-ttu-id="7943d-103">Cria um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-103">Creates an application gateway.</span></span>

## <span data-ttu-id="7943d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7943d-104">SYNTAX</span></span>

```
New-AzureApplicationGateway -Name <String> -VnetName <String>
 -Subnets <System.Collections.Generic.List`1[System.String]> [-InstanceCount <UInt32>] [-GatewaySize <String>]
 [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7943d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7943d-105">DESCRIPTION</span></span>
<span data-ttu-id="7943d-106">O cmdlet **New-AzureApplicationGateway** cria um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-106">The **New-AzureApplicationGateway** cmdlet creates an application gateway.</span></span>

## <span data-ttu-id="7943d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7943d-107">EXAMPLES</span></span>

### <span data-ttu-id="7943d-108">Exemplo 1: criar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7943d-108">Example 1: Create an application gateway</span></span>
```
PS C:\> New-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork17" -Subnets @("Subnet01", "Subnet02", "Subnet03")
```

<span data-ttu-id="7943d-109">Esse comando cria um aplicativo gateway chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="7943d-109">This command creates an application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="7943d-110">O comando implanta o gateway no VirtualNetwork17 e nas sub-redes especificadas.</span><span class="sxs-lookup"><span data-stu-id="7943d-110">The command deploys the gateway in VirtualNetwork17 and in the specified subnets.</span></span>

## <span data-ttu-id="7943d-111">OS</span><span class="sxs-lookup"><span data-stu-id="7943d-111">PARAMETERS</span></span>

### <span data-ttu-id="7943d-112">-Descrição</span><span class="sxs-lookup"><span data-stu-id="7943d-112">-Description</span></span>
<span data-ttu-id="7943d-113">Especifica uma descrição que esse cmdlet atribui ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-113">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-114">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="7943d-114">-GatewaySize</span></span>
<span data-ttu-id="7943d-115">Especifica o tamanho que esse cmdlet atribui ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-115">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="7943d-116">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="7943d-116">Valid values are:</span></span>

- <span data-ttu-id="7943d-117">Versalete</span><span class="sxs-lookup"><span data-stu-id="7943d-117">Small</span></span>
- <span data-ttu-id="7943d-118">Port</span><span class="sxs-lookup"><span data-stu-id="7943d-118">Medium</span></span>
- <span data-ttu-id="7943d-119">Muita</span><span class="sxs-lookup"><span data-stu-id="7943d-119">Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-120">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="7943d-120">-InstanceCount</span></span>
<span data-ttu-id="7943d-121">Especifica o número de instâncias atribuídas por esse cmdlet ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-121">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7943d-122">-Name</span></span>
<span data-ttu-id="7943d-123">Especifica um nome para o novo gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-123">Specifies a name for the new application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="7943d-124">-Profile</span></span>
<span data-ttu-id="7943d-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="7943d-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7943d-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="7943d-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7943d-127">-Sub-redes</span><span class="sxs-lookup"><span data-stu-id="7943d-127">-Subnets</span></span>
<span data-ttu-id="7943d-128">Especifica uma matriz de sub-redes em que esse cmdlet implanta o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="7943d-128">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-129">-VnetName</span><span class="sxs-lookup"><span data-stu-id="7943d-129">-VnetName</span></span>
<span data-ttu-id="7943d-130">Especifica a rede virtual na qual esse cmdlet implanta o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7943d-130">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7943d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7943d-131">CommonParameters</span></span>
<span data-ttu-id="7943d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7943d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7943d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7943d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7943d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7943d-134">INPUTS</span></span>

### <span data-ttu-id="7943d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7943d-135">System.String</span></span>

## <span data-ttu-id="7943d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7943d-136">OUTPUTS</span></span>

### <span data-ttu-id="7943d-137">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7943d-137">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="7943d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7943d-138">NOTES</span></span>

## <span data-ttu-id="7943d-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7943d-139">RELATED LINKS</span></span>

[<span data-ttu-id="7943d-140">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-140">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="7943d-141">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-141">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="7943d-142">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-142">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="7943d-143">Parar-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-143">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="7943d-144">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7943d-144">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
