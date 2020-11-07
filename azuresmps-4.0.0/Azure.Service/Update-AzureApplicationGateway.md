---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: C7F08804-E177-4BC5-8F0E-DEC1B467C4BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20cb37fbba8fd3789c0932f9ff1e9352334662e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945844"
---
# <span data-ttu-id="13738-101">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-101">Update-AzureApplicationGateway</span></span>

## <span data-ttu-id="13738-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13738-102">SYNOPSIS</span></span>
<span data-ttu-id="13738-103">Atualiza um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13738-103">Updates an application gateway.</span></span>

## <span data-ttu-id="13738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13738-104">SYNTAX</span></span>

```
Update-AzureApplicationGateway -Name <String> [-VnetName <String>]
 [-Subnets <System.Collections.Generic.List`1[System.String]>] [-InstanceCount <UInt32>]
 [-GatewaySize <String>] [-Description <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="13738-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13738-105">DESCRIPTION</span></span>
<span data-ttu-id="13738-106">O cmdlet **Update-AzureApplicationGateway** atualiza um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="13738-106">The **Update-AzureApplicationGateway** cmdlet updates an existing application gateway.</span></span>

## <span data-ttu-id="13738-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13738-107">EXAMPLES</span></span>

### <span data-ttu-id="13738-108">Exemplo 1: modificar um gateway do aplicativo usando seu nome</span><span class="sxs-lookup"><span data-stu-id="13738-108">Example 1: Modify an application gateway by using its name</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -VnetName "VirutalNetwork18" -Subnets @("Subnet05", "Subnet06")
```

<span data-ttu-id="13738-109">O primeiro comando interrompe o aplicativo gateway chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="13738-109">The first command stops the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="13738-110">Um gateway de aplicativo deve ser interrompido para que você possa modificar a rede virtual ou sub-redes.</span><span class="sxs-lookup"><span data-stu-id="13738-110">An application gateway must be stopped before you can modify the virtual network or subnets.</span></span>

<span data-ttu-id="13738-111">O segundo comando modifica a sub-rede virtual e sub-redes do gateway do aplicativo chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="13738-111">The second command modifies the virtual subnet and subnets for the application gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="13738-112">Exemplo 2: modificar as propriedades adicionais de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="13738-112">Example 2: Modify additional properties of an application gateway</span></span>
```
PS C:\> Update-AzureApplicationGateway -Name "ApplicationGateway06" -InstanceCount 2 -GatewaySize "Large" -Description "Updated application gateway"
```

<span data-ttu-id="13738-113">Esse comando modifica a contagem de instâncias, o tamanho do gateway e a descrição do gateway do aplicativo chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="13738-113">This command modifies the instance count, gateway size, and description for the application gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="13738-114">Esse comando não modifica a rede virtual ou sub-redes do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13738-114">This command does not modify the virtual network or subnets for the application gateway.</span></span>
<span data-ttu-id="13738-115">Portanto, você não precisa parar o gateway do aplicativo antes de executar esse comando.</span><span class="sxs-lookup"><span data-stu-id="13738-115">Therefore, you do not have to stop the application gateway before you run this command.</span></span>

### <span data-ttu-id="13738-116">Exemplo 3: modificar um gateway do aplicativo usando o pipeline</span><span class="sxs-lookup"><span data-stu-id="13738-116">Example 3: Modify an application gateway by using the pipeline</span></span>
```
PS C:\> $ApplicationGateway = Get-AzureApplicationGateway -Name "ApplicationGateway06"
PS C:\> $ApplicationGateway.GatewaySize = "Medium"
PS C:\> $ApplicationGateway | Update-AzureApplicationGateway
```

<span data-ttu-id="13738-117">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway06 usando o cmdlet **Get-AzureApplicationGateway** .</span><span class="sxs-lookup"><span data-stu-id="13738-117">The first command gets the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGateway** cmdlet.</span></span>
<span data-ttu-id="13738-118">O comando o armazena na variável $ApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="13738-118">The command stores it in the $ApplicationGateway variable.</span></span>

<span data-ttu-id="13738-119">O segundo comando atribui à propriedade **GatewaySize** o valor Medium.</span><span class="sxs-lookup"><span data-stu-id="13738-119">The second command assigns the **GatewaySize** property the value Medium.</span></span>

<span data-ttu-id="13738-120">O comando final passa o $ApplicationGateway atualizado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="13738-120">The final command passes the updated $ApplicationGateway to the current cmdlet.</span></span>

## <span data-ttu-id="13738-121">OS</span><span class="sxs-lookup"><span data-stu-id="13738-121">PARAMETERS</span></span>

### <span data-ttu-id="13738-122">-Descrição</span><span class="sxs-lookup"><span data-stu-id="13738-122">-Description</span></span>
<span data-ttu-id="13738-123">Especifica uma descrição que esse cmdlet atribui ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13738-123">Specifies a description that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="13738-124">-GatewaySize</span><span class="sxs-lookup"><span data-stu-id="13738-124">-GatewaySize</span></span>
<span data-ttu-id="13738-125">Especifica o tamanho que esse cmdlet atribui ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13738-125">Specifies the size that this cmdlet assigns to the application gateway.</span></span>
<span data-ttu-id="13738-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="13738-126">Valid values are:</span></span>

- <span data-ttu-id="13738-127">Versalete</span><span class="sxs-lookup"><span data-stu-id="13738-127">Small</span></span>
- <span data-ttu-id="13738-128">Port</span><span class="sxs-lookup"><span data-stu-id="13738-128">Medium</span></span>
- <span data-ttu-id="13738-129">Muita</span><span class="sxs-lookup"><span data-stu-id="13738-129">Large</span></span>

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

### <span data-ttu-id="13738-130">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="13738-130">-InstanceCount</span></span>
<span data-ttu-id="13738-131">Especifica o número de instâncias atribuídas por esse cmdlet ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13738-131">Specifies the number of instances that this cmdlet assigns to the application gateway.</span></span>

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

### <span data-ttu-id="13738-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="13738-132">-Name</span></span>
<span data-ttu-id="13738-133">Especifica o nome do aplicativo do gateway que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="13738-133">Specifies the name of the application gateway that this cmdlet updates.</span></span>

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

### <span data-ttu-id="13738-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="13738-134">-Profile</span></span>
<span data-ttu-id="13738-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="13738-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="13738-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="13738-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="13738-137">-Sub-redes</span><span class="sxs-lookup"><span data-stu-id="13738-137">-Subnets</span></span>
<span data-ttu-id="13738-138">Especifica uma matriz de sub-redes em que esse cmdlet implanta o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13738-138">Specifies an array of subnets in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="13738-139">Você não pode atualizar sub-redes enquanto o gateway do aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="13738-139">You cannot update subnets while the application gateway is running.</span></span>
<span data-ttu-id="13738-140">Para interromper o gateway do aplicativo, use o cmdlet Stop-AzureApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="13738-140">To stop the application gateway, use the Stop-AzureApplicationGateway cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13738-141">-VnetName</span><span class="sxs-lookup"><span data-stu-id="13738-141">-VnetName</span></span>
<span data-ttu-id="13738-142">Especifica a rede virtual na qual esse cmdlet implanta o gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="13738-142">Specifies the virtual network in which this cmdlet deploys the application gateway.</span></span>

<span data-ttu-id="13738-143">Você não pode atualizar uma rede virtual enquanto o gateway do aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="13738-143">You cannot update a virtual network while the application gateway is running.</span></span>
<span data-ttu-id="13738-144">Para interromper o gateway do aplicativo, use **Stop-AzureApplicationGateway**.</span><span class="sxs-lookup"><span data-stu-id="13738-144">To stop the application gateway, use **Stop-AzureApplicationGateway**.</span></span>

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

### <span data-ttu-id="13738-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13738-145">CommonParameters</span></span>
<span data-ttu-id="13738-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13738-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13738-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13738-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13738-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13738-148">INPUTS</span></span>

### <span data-ttu-id="13738-149">System. String</span><span class="sxs-lookup"><span data-stu-id="13738-149">System.String</span></span>

## <span data-ttu-id="13738-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13738-150">OUTPUTS</span></span>

### <span data-ttu-id="13738-151">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="13738-151">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="13738-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13738-152">NOTES</span></span>

## <span data-ttu-id="13738-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13738-153">RELATED LINKS</span></span>

[<span data-ttu-id="13738-154">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-154">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="13738-155">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-155">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="13738-156">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-156">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="13738-157">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-157">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="13738-158">Parar-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13738-158">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)
