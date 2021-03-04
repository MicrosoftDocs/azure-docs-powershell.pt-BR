---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 27eecabc9bb144270b86a26e5128b9a0d63d346b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887834"
---
# <span data-ttu-id="80965-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="80965-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="80965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80965-102">SYNOPSIS</span></span>
<span data-ttu-id="80965-103">Atualiza os metadados de um Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="80965-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="80965-104">O padrão comum para modificar uma propriedade é recuperar os metadados e os metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo do Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="80965-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="80965-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="80965-105">SYNTAX</span></span>

### <span data-ttu-id="80965-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80965-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80965-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="80965-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="80965-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="80965-108">DESCRIPTION</span></span>
<span data-ttu-id="80965-109">Atualiza os metadados de um Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="80965-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="80965-110">O padrão comum para modificar uma propriedade é recuperar os metadados e os metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo do Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="80965-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="80965-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80965-111">EXAMPLES</span></span>

### <span data-ttu-id="80965-112">Exemplo 1: atualizar um serviço de IoT do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="80965-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="80965-113">Este comando atualiza um serviço de IoT do Windows pelo nome.</span><span class="sxs-lookup"><span data-stu-id="80965-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="80965-114">Exemplo 2: atualizar um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="80965-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="80965-115">Este comando atualiza um serviço de IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="80965-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="80965-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="80965-116">PARAMETERS</span></span>

### <span data-ttu-id="80965-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="80965-117">-AdminDomainName</span></span>
<span data-ttu-id="80965-118">Domínio do Windows IoT Device Service OEM AAD</span><span class="sxs-lookup"><span data-stu-id="80965-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="80965-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="80965-119">-BillingDomainName</span></span>
<span data-ttu-id="80965-120">Domínio do Windows IoT Device Service ODM AAD</span><span class="sxs-lookup"><span data-stu-id="80965-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="80965-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80965-121">-DefaultProfile</span></span>
<span data-ttu-id="80965-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80965-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80965-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="80965-123">-Etag</span></span>
<span data-ttu-id="80965-124">O campo Etag *não é* obrigatório.</span><span class="sxs-lookup"><span data-stu-id="80965-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="80965-125">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um header de acordo com a convenção ETag normal.</span><span class="sxs-lookup"><span data-stu-id="80965-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="80965-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="80965-126">-IfMatch</span></span>
<span data-ttu-id="80965-127">ETag do Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="80965-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="80965-128">Não especifique para criar um Serviço de Dispositivo Windows IoT novo.</span><span class="sxs-lookup"><span data-stu-id="80965-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="80965-129">Necessário para atualizar um Serviço de Dispositivo Windows IoT existente.</span><span class="sxs-lookup"><span data-stu-id="80965-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="80965-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80965-130">-InputObject</span></span>
<span data-ttu-id="80965-131">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="80965-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="80965-132">-Location</span><span class="sxs-lookup"><span data-stu-id="80965-132">-Location</span></span>
<span data-ttu-id="80965-133">A região do Azure onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="80965-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="80965-134">-Name</span><span class="sxs-lookup"><span data-stu-id="80965-134">-Name</span></span>
<span data-ttu-id="80965-135">O nome do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="80965-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="80965-136">-Observação</span><span class="sxs-lookup"><span data-stu-id="80965-136">-Note</span></span>
<span data-ttu-id="80965-137">Observações do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="80965-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="80965-138">-Quantity</span><span class="sxs-lookup"><span data-stu-id="80965-138">-Quantity</span></span>
<span data-ttu-id="80965-139">Alocação de dispositivos do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="80965-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="80965-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80965-140">-ResourceGroupName</span></span>
<span data-ttu-id="80965-141">O nome do grupo de recursos que contém o Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="80965-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="80965-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80965-142">-SubscriptionId</span></span>
<span data-ttu-id="80965-143">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="80965-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="80965-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="80965-144">-Tag</span></span>
<span data-ttu-id="80965-145">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="80965-145">Resource tags.</span></span>

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

### <span data-ttu-id="80965-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80965-146">-Confirm</span></span>
<span data-ttu-id="80965-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80965-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80965-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80965-148">-WhatIf</span></span>
<span data-ttu-id="80965-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="80965-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80965-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80965-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80965-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80965-151">CommonParameters</span></span>
<span data-ttu-id="80965-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80965-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80965-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80965-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80965-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80965-154">INPUTS</span></span>

### <span data-ttu-id="80965-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="80965-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="80965-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="80965-156">OUTPUTS</span></span>

### <span data-ttu-id="80965-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="80965-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="80965-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="80965-158">NOTES</span></span>

<span data-ttu-id="80965-159">ALIASES</span><span class="sxs-lookup"><span data-stu-id="80965-159">ALIASES</span></span>

<span data-ttu-id="80965-160">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="80965-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="80965-161">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="80965-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80965-162">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="80965-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="80965-163">INPUTOBJECT <IWindowsIotServicesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="80965-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="80965-164">`[DeviceName <String>]`: O nome do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="80965-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="80965-165">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="80965-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80965-166">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="80965-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="80965-167">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="80965-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="80965-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80965-168">RELATED LINKS</span></span>

