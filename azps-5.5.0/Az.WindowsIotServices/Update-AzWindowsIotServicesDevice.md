---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118483"
---
# <span data-ttu-id="67daf-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="67daf-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="67daf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67daf-102">SYNOPSIS</span></span>
<span data-ttu-id="67daf-103">Atualiza os metadados de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="67daf-104">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="67daf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67daf-105">SYNTAX</span></span>

### <span data-ttu-id="67daf-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="67daf-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="67daf-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="67daf-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="67daf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="67daf-108">DESCRIPTION</span></span>
<span data-ttu-id="67daf-109">Atualiza os metadados de um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="67daf-110">O padrão normal para modificar uma propriedade é recuperar os metadados de segurança e metadados de segurança do Windows IoT Device Service e combiná-los com os valores modificados em um novo corpo para atualizar o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="67daf-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67daf-111">EXAMPLES</span></span>

### <span data-ttu-id="67daf-112">Exemplo 1: Atualizar um serviço windows IoT por nome</span><span class="sxs-lookup"><span data-stu-id="67daf-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="67daf-113">Este comando atualiza os serviços de IoT do Windows por nome.</span><span class="sxs-lookup"><span data-stu-id="67daf-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="67daf-114">Exemplo 2: Atualizar um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="67daf-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="67daf-115">Este comando atualiza os serviços de IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="67daf-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="67daf-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67daf-116">PARAMETERS</span></span>

### <span data-ttu-id="67daf-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="67daf-117">-AdminDomainName</span></span>
<span data-ttu-id="67daf-118">Domínio AAD do Serviço de Dispositivo IoT do Windows IoT</span><span class="sxs-lookup"><span data-stu-id="67daf-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="67daf-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="67daf-119">-BillingDomainName</span></span>
<span data-ttu-id="67daf-120">Domínio AAD do Serviço de Dispositivo do Windows IoT</span><span class="sxs-lookup"><span data-stu-id="67daf-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="67daf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67daf-121">-DefaultProfile</span></span>
<span data-ttu-id="67daf-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67daf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67daf-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="67daf-123">-Etag</span></span>
<span data-ttu-id="67daf-124">O campo Etag *não é* obrigatório.</span><span class="sxs-lookup"><span data-stu-id="67daf-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="67daf-125">Se for fornecido no corpo da resposta, ele também deverá ser fornecido como um header de acordo com a convenção ETag normal.</span><span class="sxs-lookup"><span data-stu-id="67daf-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="67daf-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="67daf-126">-IfMatch</span></span>
<span data-ttu-id="67daf-127">ETag do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="67daf-128">Não especifique para a criação de um novo Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="67daf-129">Necessário para atualizar um Serviço de Dispositivo Windows IoT existente.</span><span class="sxs-lookup"><span data-stu-id="67daf-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="67daf-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67daf-130">-InputObject</span></span>
<span data-ttu-id="67daf-131">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="67daf-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="67daf-132">-Local</span><span class="sxs-lookup"><span data-stu-id="67daf-132">-Location</span></span>
<span data-ttu-id="67daf-133">A região do Azure onde o recurso reside</span><span class="sxs-lookup"><span data-stu-id="67daf-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="67daf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="67daf-134">-Name</span></span>
<span data-ttu-id="67daf-135">O nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="67daf-136">-Observação</span><span class="sxs-lookup"><span data-stu-id="67daf-136">-Note</span></span>
<span data-ttu-id="67daf-137">Anotações do Serviço de Dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="67daf-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="67daf-138">-Quantidade</span><span class="sxs-lookup"><span data-stu-id="67daf-138">-Quantity</span></span>
<span data-ttu-id="67daf-139">Alocação de dispositivos do Windows IoT Device Service,</span><span class="sxs-lookup"><span data-stu-id="67daf-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="67daf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67daf-140">-ResourceGroupName</span></span>
<span data-ttu-id="67daf-141">O nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="67daf-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67daf-142">-SubscriptionId</span></span>
<span data-ttu-id="67daf-143">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="67daf-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="67daf-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="67daf-144">-Tag</span></span>
<span data-ttu-id="67daf-145">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="67daf-145">Resource tags.</span></span>

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

### <span data-ttu-id="67daf-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="67daf-146">-Confirm</span></span>
<span data-ttu-id="67daf-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67daf-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67daf-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67daf-148">-WhatIf</span></span>
<span data-ttu-id="67daf-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="67daf-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67daf-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67daf-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67daf-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67daf-151">CommonParameters</span></span>
<span data-ttu-id="67daf-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67daf-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67daf-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67daf-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67daf-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="67daf-154">INPUTS</span></span>

### <span data-ttu-id="67daf-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="67daf-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="67daf-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="67daf-156">OUTPUTS</span></span>

### <span data-ttu-id="67daf-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="67daf-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="67daf-158">Notas</span><span class="sxs-lookup"><span data-stu-id="67daf-158">NOTES</span></span>

<span data-ttu-id="67daf-159">Aliases</span><span class="sxs-lookup"><span data-stu-id="67daf-159">ALIASES</span></span>

<span data-ttu-id="67daf-160">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="67daf-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="67daf-161">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="67daf-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="67daf-162">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="67daf-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="67daf-163">INPUTOBJECT: <IWindowsIotServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="67daf-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="67daf-164">`[DeviceName <String>]`: o nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="67daf-165">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="67daf-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="67daf-166">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="67daf-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="67daf-167">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="67daf-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="67daf-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67daf-168">RELATED LINKS</span></span>

