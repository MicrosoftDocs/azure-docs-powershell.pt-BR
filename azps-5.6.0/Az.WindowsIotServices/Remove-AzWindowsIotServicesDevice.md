---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: e0012bab0679a49e0ad5a117845ca9e0e5d5a6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887835"
---
# <span data-ttu-id="4016d-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="4016d-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="4016d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4016d-102">SYNOPSIS</span></span>
<span data-ttu-id="4016d-103">Exclua um Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="4016d-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="4016d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4016d-104">SYNTAX</span></span>

### <span data-ttu-id="4016d-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4016d-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4016d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4016d-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4016d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4016d-107">DESCRIPTION</span></span>
<span data-ttu-id="4016d-108">Exclua um Serviço de Dispositivo windows IoT.</span><span class="sxs-lookup"><span data-stu-id="4016d-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="4016d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4016d-109">EXAMPLES</span></span>

### <span data-ttu-id="4016d-110">Exemplo 1: Remover um serviço de IoT do Windows pelo nome</span><span class="sxs-lookup"><span data-stu-id="4016d-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="4016d-111">Este comando remove um serviço de IoT do Windows pelo nome.</span><span class="sxs-lookup"><span data-stu-id="4016d-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="4016d-112">Exemplo 2: Remover um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="4016d-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="4016d-113">Este comando remove um serviço de IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="4016d-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="4016d-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4016d-114">PARAMETERS</span></span>

### <span data-ttu-id="4016d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4016d-115">-DefaultProfile</span></span>
<span data-ttu-id="4016d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4016d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4016d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4016d-117">-InputObject</span></span>
<span data-ttu-id="4016d-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4016d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4016d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4016d-119">-Name</span></span>
<span data-ttu-id="4016d-120">O nome do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="4016d-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="4016d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4016d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4016d-122">O nome do grupo de recursos que contém o Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="4016d-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="4016d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4016d-123">-SubscriptionId</span></span>
<span data-ttu-id="4016d-124">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4016d-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="4016d-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4016d-125">-Confirm</span></span>
<span data-ttu-id="4016d-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4016d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4016d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4016d-127">-WhatIf</span></span>
<span data-ttu-id="4016d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4016d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4016d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4016d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4016d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4016d-130">CommonParameters</span></span>
<span data-ttu-id="4016d-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4016d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4016d-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4016d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4016d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4016d-133">INPUTS</span></span>

### <span data-ttu-id="4016d-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="4016d-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="4016d-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4016d-135">OUTPUTS</span></span>

### <span data-ttu-id="4016d-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="4016d-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="4016d-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="4016d-137">NOTES</span></span>

<span data-ttu-id="4016d-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4016d-138">ALIASES</span></span>

<span data-ttu-id="4016d-139">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4016d-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4016d-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4016d-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4016d-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4016d-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4016d-142">INPUTOBJECT <IWindowsIotServicesIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4016d-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4016d-143">`[DeviceName <String>]`: O nome do Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="4016d-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="4016d-144">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4016d-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4016d-145">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o Windows IoT Device Service.</span><span class="sxs-lookup"><span data-stu-id="4016d-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="4016d-146">`[SubscriptionId <String>]`: O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="4016d-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4016d-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4016d-147">RELATED LINKS</span></span>

