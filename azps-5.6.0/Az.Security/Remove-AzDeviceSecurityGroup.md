---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: 302e4b096c3a41c6dd5a57a87d23bf15b83c96a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889403"
---
# <span data-ttu-id="9327a-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9327a-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="9327a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9327a-102">SYNOPSIS</span></span>
<span data-ttu-id="9327a-103">Excluir grupo de segurança de dispositivo</span><span class="sxs-lookup"><span data-stu-id="9327a-103">Delete device security group</span></span>

## <span data-ttu-id="9327a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9327a-104">SYNTAX</span></span>

### <span data-ttu-id="9327a-105">ResourceIdLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9327a-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9327a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9327a-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9327a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9327a-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9327a-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9327a-108">DESCRIPTION</span></span>
<span data-ttu-id="9327a-109">O cmdlet Remove-AzDeviceSecurityGroup exclui um grupo de segurança de dispositivo definido na solução de segurança iot.</span><span class="sxs-lookup"><span data-stu-id="9327a-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="9327a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9327a-110">EXAMPLES</span></span>

### <span data-ttu-id="9327a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9327a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="9327a-112">Excluir o grupo de segurança de dispositivo "MySecurityGroup" do hub iot com id de recurso "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="9327a-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="9327a-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9327a-113">PARAMETERS</span></span>

### <span data-ttu-id="9327a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9327a-114">-DefaultProfile</span></span>
<span data-ttu-id="9327a-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9327a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9327a-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="9327a-116">-HubResourceId</span></span>
<span data-ttu-id="9327a-117">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="9327a-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9327a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9327a-118">-InputObject</span></span>
<span data-ttu-id="9327a-119">Objeto Input.</span><span class="sxs-lookup"><span data-stu-id="9327a-119">Input Object.</span></span>

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

### <span data-ttu-id="9327a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9327a-120">-Name</span></span>
<span data-ttu-id="9327a-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="9327a-121">Resource name.</span></span>

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

### <span data-ttu-id="9327a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9327a-122">-PassThru</span></span>
<span data-ttu-id="9327a-123">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9327a-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9327a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9327a-124">-ResourceId</span></span>
<span data-ttu-id="9327a-125">ID do recurso de segurança em que você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="9327a-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9327a-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9327a-126">-Confirm</span></span>
<span data-ttu-id="9327a-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9327a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9327a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9327a-128">-WhatIf</span></span>
<span data-ttu-id="9327a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9327a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9327a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9327a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9327a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9327a-131">CommonParameters</span></span>
<span data-ttu-id="9327a-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9327a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9327a-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9327a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9327a-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9327a-134">INPUTS</span></span>

### <span data-ttu-id="9327a-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9327a-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="9327a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9327a-136">System.String</span></span>

## <span data-ttu-id="9327a-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9327a-137">OUTPUTS</span></span>

### <span data-ttu-id="9327a-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9327a-138">System.Boolean</span></span>

## <span data-ttu-id="9327a-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="9327a-139">NOTES</span></span>

## <span data-ttu-id="9327a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9327a-140">RELATED LINKS</span></span>
