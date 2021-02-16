---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118484"
---
# <span data-ttu-id="88896-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="88896-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="88896-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88896-102">SYNOPSIS</span></span>
<span data-ttu-id="88896-103">Exclua um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="88896-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88896-104">SYNTAX</span></span>

### <span data-ttu-id="88896-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="88896-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88896-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="88896-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88896-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="88896-107">DESCRIPTION</span></span>
<span data-ttu-id="88896-108">Exclua um Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="88896-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="88896-109">EXAMPLES</span></span>

### <span data-ttu-id="88896-110">Exemplo 1: remover um serviço de IoT do Windows por nome</span><span class="sxs-lookup"><span data-stu-id="88896-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="88896-111">Esse comando remove um serviço de IoT do Windows por nome.</span><span class="sxs-lookup"><span data-stu-id="88896-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="88896-112">Exemplo 2: Remover um serviço de IoT do Windows por pipeline</span><span class="sxs-lookup"><span data-stu-id="88896-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="88896-113">Esse comando remove os serviços de IoT do Windows por pipeline.</span><span class="sxs-lookup"><span data-stu-id="88896-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="88896-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88896-114">PARAMETERS</span></span>

### <span data-ttu-id="88896-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88896-115">-DefaultProfile</span></span>
<span data-ttu-id="88896-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88896-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88896-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88896-117">-InputObject</span></span>
<span data-ttu-id="88896-118">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="88896-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88896-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="88896-119">-Name</span></span>
<span data-ttu-id="88896-120">O nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="88896-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88896-121">-ResourceGroupName</span></span>
<span data-ttu-id="88896-122">O nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="88896-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88896-123">-SubscriptionId</span></span>
<span data-ttu-id="88896-124">O identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="88896-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="88896-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="88896-125">-Confirm</span></span>
<span data-ttu-id="88896-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88896-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88896-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88896-127">-WhatIf</span></span>
<span data-ttu-id="88896-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="88896-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88896-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88896-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88896-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88896-130">CommonParameters</span></span>
<span data-ttu-id="88896-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88896-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88896-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88896-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88896-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="88896-133">INPUTS</span></span>

### <span data-ttu-id="88896-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="88896-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="88896-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="88896-135">OUTPUTS</span></span>

### <span data-ttu-id="88896-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="88896-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="88896-137">Notas</span><span class="sxs-lookup"><span data-stu-id="88896-137">NOTES</span></span>

<span data-ttu-id="88896-138">Aliases</span><span class="sxs-lookup"><span data-stu-id="88896-138">ALIASES</span></span>

<span data-ttu-id="88896-139">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="88896-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88896-140">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="88896-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88896-141">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88896-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88896-142">INPUTOBJECT: <IWindowsIotServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="88896-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88896-143">`[DeviceName <String>]`: o nome do Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="88896-144">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="88896-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88896-145">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o Serviço de Dispositivo Windows IoT.</span><span class="sxs-lookup"><span data-stu-id="88896-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="88896-146">`[SubscriptionId <String>]`: o identificador de assinatura.</span><span class="sxs-lookup"><span data-stu-id="88896-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="88896-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88896-147">RELATED LINKS</span></span>

