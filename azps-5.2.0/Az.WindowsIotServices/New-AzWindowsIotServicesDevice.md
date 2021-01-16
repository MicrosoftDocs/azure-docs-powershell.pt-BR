---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260591"
---
# <span data-ttu-id="83606-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="83606-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="83606-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83606-102">SYNOPSIS</span></span>
<span data-ttu-id="83606-103">Criar ou atualizar os metadados de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="83606-104">O padrão usual para modificar uma propriedade é recuperar os metadados do serviço de dispositivo Windows IoT e os metadados de segurança e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="83606-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83606-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83606-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83606-106">DESCRIPTION</span></span>
<span data-ttu-id="83606-107">Criar ou atualizar os metadados de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="83606-108">O padrão usual para modificar uma propriedade é recuperar os metadados do serviço de dispositivo Windows IoT e os metadados de segurança e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="83606-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83606-109">EXAMPLES</span></span>

### <span data-ttu-id="83606-110">Exemplo 1: criar um novo serviço Windows IoT</span><span class="sxs-lookup"><span data-stu-id="83606-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="83606-111">Esse comando cria um novo serviço IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="83606-112">OS</span><span class="sxs-lookup"><span data-stu-id="83606-112">PARAMETERS</span></span>

### <span data-ttu-id="83606-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="83606-113">-AdminDomainName</span></span>
<span data-ttu-id="83606-114">Domínio AAD OEM do serviço de dispositivo Windows IoT</span><span class="sxs-lookup"><span data-stu-id="83606-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="83606-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="83606-115">-BillingDomainName</span></span>
<span data-ttu-id="83606-116">Domínio ODM AAD do serviço de dispositivo IoT do Windows</span><span class="sxs-lookup"><span data-stu-id="83606-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="83606-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83606-117">-DefaultProfile</span></span>
<span data-ttu-id="83606-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="83606-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83606-119">-ETag</span><span class="sxs-lookup"><span data-stu-id="83606-119">-Etag</span></span>
<span data-ttu-id="83606-120">O campo ETag *não* é necessário.</span><span class="sxs-lookup"><span data-stu-id="83606-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="83606-121">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um cabeçalho por convenção de ETag normal.</span><span class="sxs-lookup"><span data-stu-id="83606-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="83606-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="83606-122">-IfMatch</span></span>
<span data-ttu-id="83606-123">ETag do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="83606-124">Não especifique para criar um novo serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="83606-125">Obrigatório para atualizar um serviço de dispositivo IoT existente do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="83606-126">-Local</span><span class="sxs-lookup"><span data-stu-id="83606-126">-Location</span></span>
<span data-ttu-id="83606-127">A região do Azure na qual o recurso reside</span><span class="sxs-lookup"><span data-stu-id="83606-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="83606-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="83606-128">-Name</span></span>
<span data-ttu-id="83606-129">O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="83606-130">-Nota</span><span class="sxs-lookup"><span data-stu-id="83606-130">-Note</span></span>
<span data-ttu-id="83606-131">Anotações do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="83606-132">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="83606-132">-Quantity</span></span>
<span data-ttu-id="83606-133">Alocação de dispositivo do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="83606-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="83606-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83606-134">-ResourceGroupName</span></span>
<span data-ttu-id="83606-135">O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="83606-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="83606-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83606-136">-SubscriptionId</span></span>
<span data-ttu-id="83606-137">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="83606-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="83606-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="83606-138">-Tag</span></span>
<span data-ttu-id="83606-139">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="83606-139">Resource tags.</span></span>

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

### <span data-ttu-id="83606-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="83606-140">-Confirm</span></span>
<span data-ttu-id="83606-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83606-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83606-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83606-142">-WhatIf</span></span>
<span data-ttu-id="83606-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="83606-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83606-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="83606-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83606-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83606-145">CommonParameters</span></span>
<span data-ttu-id="83606-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83606-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83606-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83606-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83606-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83606-148">INPUTS</span></span>

## <span data-ttu-id="83606-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83606-149">OUTPUTS</span></span>

### <span data-ttu-id="83606-150">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="83606-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="83606-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83606-151">NOTES</span></span>

<span data-ttu-id="83606-152">ALIASES</span><span class="sxs-lookup"><span data-stu-id="83606-152">ALIASES</span></span>

## <span data-ttu-id="83606-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83606-153">RELATED LINKS</span></span>

