---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113979"
---
# <span data-ttu-id="3883c-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3883c-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="3883c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3883c-102">SYNOPSIS</span></span>
<span data-ttu-id="3883c-103">Excluir grupo de segurança do dispositivo</span><span class="sxs-lookup"><span data-stu-id="3883c-103">Delete device security group</span></span>

## <span data-ttu-id="3883c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3883c-104">SYNTAX</span></span>

### <span data-ttu-id="3883c-105">ResourceIdLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="3883c-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3883c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3883c-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3883c-107">Identificação</span><span class="sxs-lookup"><span data-stu-id="3883c-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3883c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3883c-108">DESCRIPTION</span></span>
<span data-ttu-id="3883c-109">O cmdlet Remove-AzDeviceSecurityGroup exclui um grupo de segurança de dispositivo definido na solução de segurança IOT.</span><span class="sxs-lookup"><span data-stu-id="3883c-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="3883c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3883c-110">EXAMPLES</span></span>

### <span data-ttu-id="3883c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3883c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="3883c-112">Excluir o grupo de segurança do dispositivo "mysecurity Group" do Hub IOT com ID do recurso "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="3883c-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="3883c-113">OS</span><span class="sxs-lookup"><span data-stu-id="3883c-113">PARAMETERS</span></span>

### <span data-ttu-id="3883c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3883c-114">-DefaultProfile</span></span>
<span data-ttu-id="3883c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3883c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3883c-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="3883c-116">-HubResourceId</span></span>
<span data-ttu-id="3883c-117">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="3883c-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3883c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3883c-118">-InputObject</span></span>
<span data-ttu-id="3883c-119">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="3883c-119">Input Object.</span></span>

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

### <span data-ttu-id="3883c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3883c-120">-Name</span></span>
<span data-ttu-id="3883c-121">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="3883c-121">Resource name.</span></span>

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

### <span data-ttu-id="3883c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3883c-122">-PassThru</span></span>
<span data-ttu-id="3883c-123">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3883c-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="3883c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3883c-124">-ResourceId</span></span>
<span data-ttu-id="3883c-125">ID do recurso de segurança no qual você deseja invocar o comando.</span><span class="sxs-lookup"><span data-stu-id="3883c-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3883c-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3883c-126">-Confirm</span></span>
<span data-ttu-id="3883c-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3883c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3883c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3883c-128">-WhatIf</span></span>
<span data-ttu-id="3883c-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3883c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3883c-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3883c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3883c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3883c-131">CommonParameters</span></span>
<span data-ttu-id="3883c-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3883c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3883c-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3883c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3883c-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3883c-134">INPUTS</span></span>

### <span data-ttu-id="3883c-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3883c-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="3883c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3883c-136">System.String</span></span>

## <span data-ttu-id="3883c-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3883c-137">OUTPUTS</span></span>

### <span data-ttu-id="3883c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3883c-138">System.Boolean</span></span>

## <span data-ttu-id="3883c-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3883c-139">NOTES</span></span>

## <span data-ttu-id="3883c-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3883c-140">RELATED LINKS</span></span>
