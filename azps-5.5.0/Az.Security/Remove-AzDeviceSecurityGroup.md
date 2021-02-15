---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118711"
---
# <span data-ttu-id="f1cef-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f1cef-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="f1cef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1cef-102">SYNOPSIS</span></span>
<span data-ttu-id="f1cef-103">Excluir grupo de segurança do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f1cef-103">Delete device security group</span></span>

## <span data-ttu-id="f1cef-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1cef-104">SYNTAX</span></span>

### <span data-ttu-id="f1cef-105">ResourceIdLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1cef-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1cef-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f1cef-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1cef-107">Resourceid</span><span class="sxs-lookup"><span data-stu-id="f1cef-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1cef-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1cef-108">DESCRIPTION</span></span>
<span data-ttu-id="f1cef-109">O cmdlet Remove-AzDeviceSecurityGroup exclui um grupo de segurança de dispositivo definido na solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="f1cef-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="f1cef-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1cef-110">EXAMPLES</span></span>

### <span data-ttu-id="f1cef-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1cef-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="f1cef-112">Excluir o grupo de segurança de dispositivo "MySecurityGroup" do hub iot com a id de recursos "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="f1cef-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="f1cef-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1cef-113">PARAMETERS</span></span>

### <span data-ttu-id="f1cef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1cef-114">-DefaultProfile</span></span>
<span data-ttu-id="f1cef-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1cef-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="f1cef-116">-HubResourceId</span></span>
<span data-ttu-id="f1cef-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="f1cef-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1cef-118">-InputObject</span></span>
<span data-ttu-id="f1cef-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="f1cef-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1cef-120">-Name</span></span>
<span data-ttu-id="f1cef-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f1cef-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1cef-122">-PassThru</span></span>
<span data-ttu-id="f1cef-123">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f1cef-123">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1cef-124">-ResourceId</span></span>
<span data-ttu-id="f1cef-125">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="f1cef-125">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1cef-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f1cef-126">-Confirm</span></span>
<span data-ttu-id="f1cef-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1cef-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1cef-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1cef-128">-WhatIf</span></span>
<span data-ttu-id="f1cef-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f1cef-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1cef-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1cef-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1cef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1cef-131">CommonParameters</span></span>
<span data-ttu-id="f1cef-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1cef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1cef-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1cef-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1cef-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="f1cef-134">INPUTS</span></span>

### <span data-ttu-id="f1cef-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f1cef-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="f1cef-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f1cef-136">System.String</span></span>

## <span data-ttu-id="f1cef-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="f1cef-137">OUTPUTS</span></span>

### <span data-ttu-id="f1cef-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f1cef-138">System.Boolean</span></span>

## <span data-ttu-id="f1cef-139">Notas</span><span class="sxs-lookup"><span data-stu-id="f1cef-139">NOTES</span></span>

## <span data-ttu-id="f1cef-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1cef-140">RELATED LINKS</span></span>
