---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427742"
---
# <span data-ttu-id="f5d00-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="f5d00-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="f5d00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5d00-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d00-103">Excluir um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f5d00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5d00-104">SYNTAX</span></span>

### <span data-ttu-id="f5d00-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5d00-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f5d00-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d00-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f5d00-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5d00-107">DESCRIPTION</span></span>
<span data-ttu-id="f5d00-108">Excluir um serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f5d00-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5d00-109">EXAMPLES</span></span>

### <span data-ttu-id="f5d00-110">Exemplo 1: remover um serviço Windows IoT por nome</span><span class="sxs-lookup"><span data-stu-id="f5d00-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="f5d00-111">Esse comando Remove um serviço Windows IoT por nome.</span><span class="sxs-lookup"><span data-stu-id="f5d00-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="f5d00-112">Exemplo 2: remover um serviço Windows IoT por pipeline</span><span class="sxs-lookup"><span data-stu-id="f5d00-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="f5d00-113">Esse comando Remove um serviço Windows IoT por pipeline.</span><span class="sxs-lookup"><span data-stu-id="f5d00-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="f5d00-114">OS</span><span class="sxs-lookup"><span data-stu-id="f5d00-114">PARAMETERS</span></span>

### <span data-ttu-id="f5d00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d00-115">-DefaultProfile</span></span>
<span data-ttu-id="f5d00-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f5d00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5d00-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5d00-117">-InputObject</span></span>
<span data-ttu-id="f5d00-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f5d00-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5d00-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5d00-119">-Name</span></span>
<span data-ttu-id="f5d00-120">O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-120">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d00-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5d00-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5d00-122">O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d00-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f5d00-123">-SubscriptionId</span></span>
<span data-ttu-id="f5d00-124">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f5d00-124">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5d00-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5d00-125">-Confirm</span></span>
<span data-ttu-id="f5d00-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5d00-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5d00-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5d00-127">-WhatIf</span></span>
<span data-ttu-id="f5d00-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5d00-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5d00-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5d00-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5d00-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d00-130">CommonParameters</span></span>
<span data-ttu-id="f5d00-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5d00-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d00-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5d00-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d00-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5d00-133">INPUTS</span></span>

### <span data-ttu-id="f5d00-134">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="f5d00-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="f5d00-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5d00-135">OUTPUTS</span></span>

### <span data-ttu-id="f5d00-136">Microsoft. Azure. PowerShell. cmdlets. WindowsIotServices. Models. Api20190601. IDeviceService</span><span class="sxs-lookup"><span data-stu-id="f5d00-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="f5d00-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5d00-137">NOTES</span></span>

<span data-ttu-id="f5d00-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f5d00-138">ALIASES</span></span>

<span data-ttu-id="f5d00-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f5d00-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f5d00-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f5d00-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f5d00-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f5d00-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f5d00-142">INPUTobject <IWindowsIotServicesIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f5d00-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f5d00-143">`[DeviceName <String>]`: O nome do serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f5d00-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f5d00-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f5d00-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o serviço de dispositivo IoT do Windows.</span><span class="sxs-lookup"><span data-stu-id="f5d00-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f5d00-146">`[SubscriptionId <String>]`: O identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f5d00-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="f5d00-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5d00-147">RELATED LINKS</span></span>

