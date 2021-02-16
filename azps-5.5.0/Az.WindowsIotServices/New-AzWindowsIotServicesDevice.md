---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118485"
---
# <span data-ttu-id="3bb4f-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="3bb4f-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="3bb4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bb4f-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb4f-103">Criar ou atualizar os metadados de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="3bb4f-104">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="3bb4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bb4f-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bb4f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="3bb4f-106">DESCRIPTION</span></span>
<span data-ttu-id="3bb4f-107">Criar ou atualizar os metadados de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="3bb4f-108">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="3bb4f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bb4f-109">EXAMPLES</span></span>

### <span data-ttu-id="3bb4f-110">Exemplo 1: Criar um novo serviço Windows IoT</span><span class="sxs-lookup"><span data-stu-id="3bb4f-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="3bb4f-111">Esse comando cria um novo serviço windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="3bb4f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bb4f-112">PARAMETERS</span></span>

### <span data-ttu-id="3bb4f-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="3bb4f-113">-AdminDomainName</span></span>
<span data-ttu-id="3bb4f-114">Domínio AAD do Serviço de Dispositivo IoT do Windows IoT</span><span class="sxs-lookup"><span data-stu-id="3bb4f-114">Windows IoT Device Service OEM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="3bb4f-115">-BillingDomainName</span></span>
<span data-ttu-id="3bb4f-116">Domínio AAD do Serviço de Dispositivo do Windows IoT</span><span class="sxs-lookup"><span data-stu-id="3bb4f-116">Windows IoT Device Service ODM AAD domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb4f-117">-DefaultProfile</span></span>
<span data-ttu-id="3bb4f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="3bb4f-119">-Etag</span></span>
<span data-ttu-id="3bb4f-120">O campo Etag *não é* obrigatório.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="3bb4f-121">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um header de acordo com a convenção ETag normal.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="3bb4f-122">-IfMatch</span></span>
<span data-ttu-id="3bb4f-123">ETag do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="3bb4f-124">Não especifique para criar um novo Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="3bb4f-125">Necessário para atualizar um Serviço de Dispositivo Windows IoT existente.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-125">Required to update an existing Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-126">-Local</span><span class="sxs-lookup"><span data-stu-id="3bb4f-126">-Location</span></span>
<span data-ttu-id="3bb4f-127">A região do Azure onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="3bb4f-127">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bb4f-128">-Name</span></span>
<span data-ttu-id="3bb4f-129">O nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-129">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-130">-Observação</span><span class="sxs-lookup"><span data-stu-id="3bb4f-130">-Note</span></span>
<span data-ttu-id="3bb4f-131">Anotações do Serviço de Dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-131">Windows IoT Device Service notes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-132">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="3bb4f-132">-Quantity</span></span>
<span data-ttu-id="3bb4f-133">Alocação de dispositivos do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="3bb4f-133">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb4f-134">-ResourceGroupName</span></span>
<span data-ttu-id="3bb4f-135">O nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3bb4f-136">-SubscriptionId</span></span>
<span data-ttu-id="3bb4f-137">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bb4f-138">-Tag</span></span>
<span data-ttu-id="3bb4f-139">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-139">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3bb4f-140">-Confirm</span></span>
<span data-ttu-id="3bb4f-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb4f-142">-WhatIf</span></span>
<span data-ttu-id="3bb4f-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb4f-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb4f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb4f-145">CommonParameters</span></span>
<span data-ttu-id="3bb4f-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb4f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb4f-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3bb4f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb4f-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="3bb4f-148">INPUTS</span></span>

## <span data-ttu-id="3bb4f-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="3bb4f-149">OUTPUTS</span></span>

### <span data-ttu-id="3bb4f-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="3bb4f-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="3bb4f-151">Notas</span><span class="sxs-lookup"><span data-stu-id="3bb4f-151">NOTES</span></span>

<span data-ttu-id="3bb4f-152">Aliases</span><span class="sxs-lookup"><span data-stu-id="3bb4f-152">ALIASES</span></span>

## <span data-ttu-id="3bb4f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bb4f-153">RELATED LINKS</span></span>

