---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602580"
---
# <span data-ttu-id="0e2fa-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="0e2fa-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="0e2fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e2fa-102">SYNOPSIS</span></span>
<span data-ttu-id="0e2fa-103">Atualiza a configuração de provisionamento automático</span><span class="sxs-lookup"><span data-stu-id="0e2fa-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e2fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e2fa-104">SYNTAX</span></span>

### <span data-ttu-id="0e2fa-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="0e2fa-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2fa-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="0e2fa-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e2fa-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e2fa-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e2fa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e2fa-108">DESCRIPTION</span></span>
<span data-ttu-id="0e2fa-109">Ativa ou desativa as configurações de provisionamento automático para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="0e2fa-110">As configurações de provisionamento automático permitem que você decida se deseja que a central de segurança do Azure forneça automaticamente um agente de segurança que será instalado em suas VMs.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="0e2fa-111">O agente de segurança monitorará sua VM para criar alertas de segurança e monitorará a conformidade de segurança da VM.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="0e2fa-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e2fa-112">EXAMPLES</span></span>

### <span data-ttu-id="0e2fa-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e2fa-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="0e2fa-114">Ativa a configuração de provisionamento automático para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="0e2fa-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0e2fa-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="0e2fa-116">Desativa a configuração automática de provisionamento para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="0e2fa-117">OS</span><span class="sxs-lookup"><span data-stu-id="0e2fa-117">PARAMETERS</span></span>

### <span data-ttu-id="0e2fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e2fa-118">-DefaultProfile</span></span>
<span data-ttu-id="0e2fa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="0e2fa-120">-EnableAutoProvision</span></span>
<span data-ttu-id="0e2fa-121">Provisionamento automático.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e2fa-122">-InputObject</span></span>
<span data-ttu-id="0e2fa-123">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e2fa-124">-Name</span></span>
<span data-ttu-id="0e2fa-125">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e2fa-126">-ResourceId</span></span>
<span data-ttu-id="0e2fa-127">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e2fa-128">-Confirm</span></span>
<span data-ttu-id="0e2fa-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e2fa-130">-WhatIf</span></span>
<span data-ttu-id="0e2fa-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e2fa-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e2fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e2fa-133">CommonParameters</span></span>
<span data-ttu-id="0e2fa-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e2fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e2fa-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e2fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e2fa-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e2fa-136">INPUTS</span></span>

### <span data-ttu-id="0e2fa-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0e2fa-137">System.String</span></span>
<span data-ttu-id="0e2fa-138">System. Management. Automation. SwitchParameter Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="0e2fa-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="0e2fa-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e2fa-139">OUTPUTS</span></span>

### <span data-ttu-id="0e2fa-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="0e2fa-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="0e2fa-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e2fa-141">NOTES</span></span>

## <span data-ttu-id="0e2fa-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e2fa-142">RELATED LINKS</span></span>
