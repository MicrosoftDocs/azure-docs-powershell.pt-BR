---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 40256025817e4f840f8d65ff8bdf6bc92c5b3d10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891543"
---
# <span data-ttu-id="ac162-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="ac162-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="ac162-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac162-102">SYNOPSIS</span></span>
<span data-ttu-id="ac162-103">Crie ou atualize os metadados de um Serviço de Dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac162-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="ac162-104">O padrão comum para modificar uma propriedade é recuperar os metadados e os metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo do Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ac162-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="ac162-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ac162-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac162-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ac162-106">DESCRIPTION</span></span>
<span data-ttu-id="ac162-107">Crie ou atualize os metadados de um Serviço de Dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac162-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="ac162-108">O padrão comum para modificar uma propriedade é recuperar os metadados e os metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo do Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ac162-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="ac162-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac162-109">EXAMPLES</span></span>

### <span data-ttu-id="ac162-110">Exemplo 1: Criar um novo serviço de IoT do Windows</span><span class="sxs-lookup"><span data-stu-id="ac162-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="ac162-111">Este comando cria um novo serviço de IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac162-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="ac162-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ac162-112">PARAMETERS</span></span>

### <span data-ttu-id="ac162-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="ac162-113">-AdminDomainName</span></span>
<span data-ttu-id="ac162-114">Domínio do Windows IoT Device Service OEM AAD</span><span class="sxs-lookup"><span data-stu-id="ac162-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="ac162-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="ac162-115">-BillingDomainName</span></span>
<span data-ttu-id="ac162-116">Domínio do Windows IoT Device Service ODM AAD</span><span class="sxs-lookup"><span data-stu-id="ac162-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="ac162-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac162-117">-DefaultProfile</span></span>
<span data-ttu-id="ac162-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac162-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac162-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="ac162-119">-Etag</span></span>
<span data-ttu-id="ac162-120">O campo Etag *não é* obrigatório.</span><span class="sxs-lookup"><span data-stu-id="ac162-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="ac162-121">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um header de acordo com a convenção ETag normal.</span><span class="sxs-lookup"><span data-stu-id="ac162-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="ac162-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="ac162-122">-IfMatch</span></span>
<span data-ttu-id="ac162-123">ETag do Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ac162-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="ac162-124">Não especifique para a criação de um novo Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="ac162-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="ac162-125">Necessário para atualizar um Serviço de Dispositivo Windows IoT existente.</span><span class="sxs-lookup"><span data-stu-id="ac162-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="ac162-126">-Location</span><span class="sxs-lookup"><span data-stu-id="ac162-126">-Location</span></span>
<span data-ttu-id="ac162-127">A região do Azure onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="ac162-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="ac162-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ac162-128">-Name</span></span>
<span data-ttu-id="ac162-129">O nome do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="ac162-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="ac162-130">-Observação</span><span class="sxs-lookup"><span data-stu-id="ac162-130">-Note</span></span>
<span data-ttu-id="ac162-131">Observações do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="ac162-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="ac162-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="ac162-132">-Quantity</span></span>
<span data-ttu-id="ac162-133">Alocação de dispositivos do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="ac162-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="ac162-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac162-134">-ResourceGroupName</span></span>
<span data-ttu-id="ac162-135">O nome do grupo de recursos que contém o Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="ac162-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="ac162-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac162-136">-SubscriptionId</span></span>
<span data-ttu-id="ac162-137">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="ac162-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="ac162-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac162-138">-Tag</span></span>
<span data-ttu-id="ac162-139">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="ac162-139">Resource tags.</span></span>

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

### <span data-ttu-id="ac162-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac162-140">-Confirm</span></span>
<span data-ttu-id="ac162-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac162-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac162-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac162-142">-WhatIf</span></span>
<span data-ttu-id="ac162-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ac162-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac162-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac162-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac162-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac162-145">CommonParameters</span></span>
<span data-ttu-id="ac162-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac162-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac162-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac162-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac162-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac162-148">INPUTS</span></span>

## <span data-ttu-id="ac162-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ac162-149">OUTPUTS</span></span>

### <span data-ttu-id="ac162-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="ac162-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="ac162-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="ac162-151">NOTES</span></span>

<span data-ttu-id="ac162-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ac162-152">ALIASES</span></span>

## <span data-ttu-id="ac162-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac162-153">RELATED LINKS</span></span>

