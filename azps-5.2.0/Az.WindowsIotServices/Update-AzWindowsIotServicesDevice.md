---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264262"
---
# <span data-ttu-id="81e70-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="81e70-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="81e70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81e70-102">SYNOPSIS</span></span>
<span data-ttu-id="81e70-103">Atualiza os metadados de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="81e70-104">O padrão usual para modificar uma propriedade é recuperar os metadados do serviço de dispositivo Windows IoT e os metadados de segurança e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="81e70-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81e70-105">SYNTAX</span></span>

### <span data-ttu-id="81e70-106">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="81e70-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="81e70-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="81e70-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="81e70-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81e70-108">DESCRIPTION</span></span>
<span data-ttu-id="81e70-109">Atualiza os metadados de um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="81e70-110">O padrão usual para modificar uma propriedade é recuperar os metadados do serviço de dispositivo Windows IoT e os metadados de segurança e, em seguida, combiná-los com os valores modificados em um novo corpo para atualizar o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="81e70-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81e70-111">EXAMPLES</span></span>

### <span data-ttu-id="81e70-112">Exemplo 1: atualizar um serviço Windows IoT por nome</span><span class="sxs-lookup"><span data-stu-id="81e70-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="81e70-113">Este comando atualiza um serviço Windows IoT por nome.</span><span class="sxs-lookup"><span data-stu-id="81e70-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="81e70-114">Exemplo 2: atualizar um serviço Windows IoT por pipeline</span><span class="sxs-lookup"><span data-stu-id="81e70-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="81e70-115">Esse comando atualiza um serviço IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="81e70-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="81e70-116">OS</span><span class="sxs-lookup"><span data-stu-id="81e70-116">PARAMETERS</span></span>

### <span data-ttu-id="81e70-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="81e70-117">-AdminDomainName</span></span>
<span data-ttu-id="81e70-118">Domínio AAD OEM do serviço de dispositivo Windows IoT</span><span class="sxs-lookup"><span data-stu-id="81e70-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="81e70-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="81e70-119">-BillingDomainName</span></span>
<span data-ttu-id="81e70-120">Domínio ODM AAD do serviço de dispositivo IoT do Windows</span><span class="sxs-lookup"><span data-stu-id="81e70-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="81e70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81e70-121">-DefaultProfile</span></span>
<span data-ttu-id="81e70-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81e70-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81e70-123">-ETag</span><span class="sxs-lookup"><span data-stu-id="81e70-123">-Etag</span></span>
<span data-ttu-id="81e70-124">O campo ETag *não* é necessário.</span><span class="sxs-lookup"><span data-stu-id="81e70-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="81e70-125">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um cabeçalho por convenção de ETag normal.</span><span class="sxs-lookup"><span data-stu-id="81e70-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="81e70-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="81e70-126">-IfMatch</span></span>
<span data-ttu-id="81e70-127">ETag do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="81e70-128">Não especifique para criar um novo serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="81e70-129">Obrigatório para atualizar um serviço de dispositivo IoT existente do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="81e70-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81e70-130">-InputObject</span></span>
<span data-ttu-id="81e70-131">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="81e70-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81e70-132">-Local</span><span class="sxs-lookup"><span data-stu-id="81e70-132">-Location</span></span>
<span data-ttu-id="81e70-133">A região do Azure na qual o recurso reside</span><span class="sxs-lookup"><span data-stu-id="81e70-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="81e70-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="81e70-134">-Name</span></span>
<span data-ttu-id="81e70-135">O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e70-136">-Nota</span><span class="sxs-lookup"><span data-stu-id="81e70-136">-Note</span></span>
<span data-ttu-id="81e70-137">Anotações do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="81e70-138">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="81e70-138">-Quantity</span></span>
<span data-ttu-id="81e70-139">Alocação de dispositivo do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="81e70-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="81e70-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81e70-140">-ResourceGroupName</span></span>
<span data-ttu-id="81e70-141">O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e70-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81e70-142">-SubscriptionId</span></span>
<span data-ttu-id="81e70-143">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="81e70-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81e70-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="81e70-144">-Tag</span></span>
<span data-ttu-id="81e70-145">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="81e70-145">Resource tags.</span></span>

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

### <span data-ttu-id="81e70-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81e70-146">-Confirm</span></span>
<span data-ttu-id="81e70-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81e70-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81e70-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81e70-148">-WhatIf</span></span>
<span data-ttu-id="81e70-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81e70-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81e70-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81e70-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81e70-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81e70-151">CommonParameters</span></span>
<span data-ttu-id="81e70-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81e70-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81e70-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81e70-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81e70-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81e70-154">INPUTS</span></span>

### <span data-ttu-id="81e70-155">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="81e70-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="81e70-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81e70-156">OUTPUTS</span></span>

### <span data-ttu-id="81e70-157">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="81e70-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="81e70-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81e70-158">NOTES</span></span>

<span data-ttu-id="81e70-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81e70-159">ALIASES</span></span>

<span data-ttu-id="81e70-160">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="81e70-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="81e70-161">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="81e70-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="81e70-162">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="81e70-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="81e70-163">INPUTobject <IWindowsIotServicesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="81e70-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="81e70-164">`[DeviceName <String>]`: O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="81e70-165">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="81e70-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="81e70-166">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="81e70-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="81e70-167">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="81e70-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="81e70-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81e70-168">RELATED LINKS</span></span>

