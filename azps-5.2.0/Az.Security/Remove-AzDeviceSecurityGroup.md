---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258928"
---
# <span data-ttu-id="37151-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="37151-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="37151-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37151-102">SYNOPSIS</span></span>
<span data-ttu-id="37151-103">Excluir grupo de segurança do dispositivo</span><span class="sxs-lookup"><span data-stu-id="37151-103">Delete device security group</span></span>

## <span data-ttu-id="37151-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37151-104">SYNTAX</span></span>

### <span data-ttu-id="37151-105">ResourceIdLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="37151-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37151-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="37151-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37151-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="37151-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37151-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37151-108">DESCRIPTION</span></span>
<span data-ttu-id="37151-109">O cmdlet Remove-AzDeviceSecurityGroup exclui um grupo de segurança de dispositivo definido na solução de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="37151-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="37151-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37151-110">EXAMPLES</span></span>

### <span data-ttu-id="37151-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37151-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="37151-112">Excluir o grupo de segurança do dispositivo "mysecurity Group" do Hub IOT com ID do recurso "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="37151-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="37151-113">OS</span><span class="sxs-lookup"><span data-stu-id="37151-113">PARAMETERS</span></span>

### <span data-ttu-id="37151-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37151-114">-DefaultProfile</span></span>
<span data-ttu-id="37151-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37151-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37151-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="37151-116">-HubResourceId</span></span>
<span data-ttu-id="37151-117">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="37151-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="37151-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37151-118">-InputObject</span></span>
<span data-ttu-id="37151-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="37151-119">Input Object.</span></span>

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

### <span data-ttu-id="37151-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="37151-120">-Name</span></span>
<span data-ttu-id="37151-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="37151-121">Resource name.</span></span>

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

### <span data-ttu-id="37151-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37151-122">-PassThru</span></span>
<span data-ttu-id="37151-123">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="37151-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="37151-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37151-124">-ResourceId</span></span>
<span data-ttu-id="37151-125">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="37151-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="37151-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37151-126">-Confirm</span></span>
<span data-ttu-id="37151-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37151-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37151-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37151-128">-WhatIf</span></span>
<span data-ttu-id="37151-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37151-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37151-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37151-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37151-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37151-131">CommonParameters</span></span>
<span data-ttu-id="37151-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37151-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37151-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37151-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37151-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37151-134">INPUTS</span></span>

### <span data-ttu-id="37151-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="37151-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="37151-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37151-136">System.String</span></span>

## <span data-ttu-id="37151-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37151-137">OUTPUTS</span></span>

### <span data-ttu-id="37151-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37151-138">System.Boolean</span></span>

## <span data-ttu-id="37151-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37151-139">NOTES</span></span>

## <span data-ttu-id="37151-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37151-140">RELATED LINKS</span></span>
