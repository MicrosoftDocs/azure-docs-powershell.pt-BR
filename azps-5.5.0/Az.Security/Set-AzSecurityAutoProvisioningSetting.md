---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112612"
---
# <span data-ttu-id="1b52e-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="1b52e-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="1b52e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b52e-102">SYNOPSIS</span></span>
<span data-ttu-id="1b52e-103">Atualiza a configuração de provisionamento automático</span><span class="sxs-lookup"><span data-stu-id="1b52e-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="1b52e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b52e-104">SYNTAX</span></span>

### <span data-ttu-id="1b52e-105">SubscriptionLevelResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b52e-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b52e-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="1b52e-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b52e-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1b52e-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b52e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1b52e-108">DESCRIPTION</span></span>
<span data-ttu-id="1b52e-109">2010 2010 2010 2010 2010 2010 2010 2010</span><span class="sxs-lookup"><span data-stu-id="1b52e-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="1b52e-110">As Configurações de Provisionamento Automático permitem que você decida se deseja que a Central de Segurança do Azure provisione automaticamente um agente de segurança que será instalado em seus VMs.</span><span class="sxs-lookup"><span data-stu-id="1b52e-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="1b52e-111">O agente de segurança monitorará seu VM para criar alertas de segurança e monitorar a conformidade de segurança do VM.</span><span class="sxs-lookup"><span data-stu-id="1b52e-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="1b52e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1b52e-112">EXAMPLES</span></span>

### <span data-ttu-id="1b52e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1b52e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="1b52e-114">2010 2010 2010 2010 2010 2010 2</span><span class="sxs-lookup"><span data-stu-id="1b52e-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="1b52e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1b52e-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="1b52e-116">Desliga a configuração de provisionamento automático para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1b52e-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="1b52e-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b52e-117">PARAMETERS</span></span>

### <span data-ttu-id="1b52e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b52e-118">-DefaultProfile</span></span>
<span data-ttu-id="1b52e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b52e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b52e-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="1b52e-120">-EnableAutoProvision</span></span>
<span data-ttu-id="1b52e-121">Provisionamento Automático.</span><span class="sxs-lookup"><span data-stu-id="1b52e-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b52e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b52e-122">-InputObject</span></span>
<span data-ttu-id="1b52e-123">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="1b52e-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b52e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b52e-124">-Name</span></span>
<span data-ttu-id="1b52e-125">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1b52e-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b52e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b52e-126">-ResourceId</span></span>
<span data-ttu-id="1b52e-127">ID do Recurso.</span><span class="sxs-lookup"><span data-stu-id="1b52e-127">Resource ID.</span></span>

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

### <span data-ttu-id="1b52e-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1b52e-128">-Confirm</span></span>
<span data-ttu-id="1b52e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b52e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b52e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b52e-130">-WhatIf</span></span>
<span data-ttu-id="1b52e-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1b52e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b52e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b52e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b52e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b52e-133">CommonParameters</span></span>
<span data-ttu-id="1b52e-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b52e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b52e-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b52e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b52e-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="1b52e-136">INPUTS</span></span>

### <span data-ttu-id="1b52e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1b52e-137">System.String</span></span>

### <span data-ttu-id="1b52e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="1b52e-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="1b52e-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="1b52e-139">OUTPUTS</span></span>

### <span data-ttu-id="1b52e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="1b52e-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="1b52e-141">Notas</span><span class="sxs-lookup"><span data-stu-id="1b52e-141">NOTES</span></span>

## <span data-ttu-id="1b52e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b52e-142">RELATED LINKS</span></span>
