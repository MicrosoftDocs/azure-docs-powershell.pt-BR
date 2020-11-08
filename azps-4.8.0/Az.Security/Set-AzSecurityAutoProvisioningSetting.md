---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110882"
---
# <span data-ttu-id="975b2-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="975b2-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="975b2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="975b2-102">SYNOPSIS</span></span>
<span data-ttu-id="975b2-103">Atualiza a configuração de provisionamento automático</span><span class="sxs-lookup"><span data-stu-id="975b2-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="975b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="975b2-104">SYNTAX</span></span>

### <span data-ttu-id="975b2-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="975b2-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975b2-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="975b2-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="975b2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="975b2-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="975b2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="975b2-108">DESCRIPTION</span></span>
<span data-ttu-id="975b2-109">Ativa ou desativa as configurações de provisionamento automático para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="975b2-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="975b2-110">As configurações de provisionamento automático permitem que você decida se deseja que a central de segurança do Azure forneça automaticamente um agente de segurança que será instalado em suas VMs.</span><span class="sxs-lookup"><span data-stu-id="975b2-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="975b2-111">O agente de segurança monitorará sua VM para criar alertas de segurança e monitorará a conformidade de segurança da VM.</span><span class="sxs-lookup"><span data-stu-id="975b2-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="975b2-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="975b2-112">EXAMPLES</span></span>

### <span data-ttu-id="975b2-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="975b2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="975b2-114">Ativa a configuração de provisionamento automático para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="975b2-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="975b2-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="975b2-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="975b2-116">Desativa a configuração automática de provisionamento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="975b2-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="975b2-117">OS</span><span class="sxs-lookup"><span data-stu-id="975b2-117">PARAMETERS</span></span>

### <span data-ttu-id="975b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="975b2-118">-DefaultProfile</span></span>
<span data-ttu-id="975b2-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="975b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="975b2-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="975b2-120">-EnableAutoProvision</span></span>
<span data-ttu-id="975b2-121">Provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="975b2-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="975b2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="975b2-122">-InputObject</span></span>
<span data-ttu-id="975b2-123">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="975b2-123">Input Object.</span></span>

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

### <span data-ttu-id="975b2-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="975b2-124">-Name</span></span>
<span data-ttu-id="975b2-125">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="975b2-125">Resource name.</span></span>

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

### <span data-ttu-id="975b2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="975b2-126">-ResourceId</span></span>
<span data-ttu-id="975b2-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="975b2-127">Resource ID.</span></span>

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

### <span data-ttu-id="975b2-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="975b2-128">-Confirm</span></span>
<span data-ttu-id="975b2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="975b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="975b2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="975b2-130">-WhatIf</span></span>
<span data-ttu-id="975b2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="975b2-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="975b2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="975b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="975b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="975b2-133">CommonParameters</span></span>
<span data-ttu-id="975b2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="975b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="975b2-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="975b2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="975b2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="975b2-136">INPUTS</span></span>

### <span data-ttu-id="975b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="975b2-137">System.String</span></span>

### <span data-ttu-id="975b2-138">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="975b2-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="975b2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="975b2-139">OUTPUTS</span></span>

### <span data-ttu-id="975b2-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="975b2-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="975b2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="975b2-141">NOTES</span></span>

## <span data-ttu-id="975b2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="975b2-142">RELATED LINKS</span></span>
