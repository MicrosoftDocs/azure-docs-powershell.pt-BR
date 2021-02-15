---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114548"
---
# <span data-ttu-id="df396-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="df396-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="df396-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df396-102">SYNOPSIS</span></span>
<span data-ttu-id="df396-103">Configure as configurações de notificação de Recuperação de Site do Azure (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="df396-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="df396-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df396-104">SYNTAX</span></span>

### <span data-ttu-id="df396-105">Definir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df396-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df396-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="df396-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df396-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="df396-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df396-108">Desativar</span><span class="sxs-lookup"><span data-stu-id="df396-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df396-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="df396-109">DESCRIPTION</span></span>
<span data-ttu-id="df396-110">O cmdlet **Set-AzRecoveryServicesAsrNotificationSetting** configura configurações de notificação de Recuperação de Site do Azure (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="df396-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="df396-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df396-111">EXAMPLES</span></span>

### <span data-ttu-id="df396-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df396-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="df396-113">Desabilitar notificação.</span><span class="sxs-lookup"><span data-stu-id="df396-113">Disable notification.</span></span>

### <span data-ttu-id="df396-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="df396-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="df396-115">Definir notificação para endereços de email personalizados e para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="df396-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="df396-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="df396-116">Example 3</span></span>

<span data-ttu-id="df396-117">Configure as configurações de notificação de Recuperação de Site do Azure (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="df396-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="df396-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="df396-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="df396-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df396-119">PARAMETERS</span></span>

### <span data-ttu-id="df396-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="df396-120">-CustomEmailAddress</span></span>
<span data-ttu-id="df396-121">Alerta/Notificação enviada para emails.</span><span class="sxs-lookup"><span data-stu-id="df396-121">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df396-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df396-122">-DefaultProfile</span></span>
<span data-ttu-id="df396-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="df396-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df396-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="df396-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="df396-125">A opção Parâmetro especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="df396-125">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df396-126">-Desabilitar Anotação</span><span class="sxs-lookup"><span data-stu-id="df396-126">-DisableNotification</span></span>
<span data-ttu-id="df396-127">Sinalizar para desabilitar todas as notificações.</span><span class="sxs-lookup"><span data-stu-id="df396-127">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df396-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="df396-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="df396-129">A opção Parâmetro especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="df396-129">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df396-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="df396-130">-LocaleID</span></span>
<span data-ttu-id="df396-131">Idioma de email de alerta /notificação para o usuário(códigos de cultura com suporte da microsoft).</span><span class="sxs-lookup"><span data-stu-id="df396-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df396-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="df396-132">-Confirm</span></span>
<span data-ttu-id="df396-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df396-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df396-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df396-134">-WhatIf</span></span>
<span data-ttu-id="df396-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="df396-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df396-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="df396-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df396-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df396-137">CommonParameters</span></span>
<span data-ttu-id="df396-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df396-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df396-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df396-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df396-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="df396-140">INPUTS</span></span>

### <span data-ttu-id="df396-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="df396-141">None</span></span>

## <span data-ttu-id="df396-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="df396-142">OUTPUTS</span></span>

### <span data-ttu-id="df396-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="df396-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="df396-144">Notas</span><span class="sxs-lookup"><span data-stu-id="df396-144">NOTES</span></span>

## <span data-ttu-id="df396-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df396-145">RELATED LINKS</span></span>
