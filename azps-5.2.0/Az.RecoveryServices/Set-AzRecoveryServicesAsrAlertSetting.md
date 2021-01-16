---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262727"
---
# <span data-ttu-id="3115e-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3115e-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="3115e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3115e-102">SYNOPSIS</span></span>
<span data-ttu-id="3115e-103">Configurar as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="3115e-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3115e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3115e-104">SYNTAX</span></span>

### <span data-ttu-id="3115e-105">Definir (padrão)</span><span class="sxs-lookup"><span data-stu-id="3115e-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3115e-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3115e-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3115e-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3115e-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3115e-108">Desabilita</span><span class="sxs-lookup"><span data-stu-id="3115e-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3115e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3115e-109">DESCRIPTION</span></span>
<span data-ttu-id="3115e-110">O cmdlet **set-AzRecoveryServicesAsrNotificationSetting** configura as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="3115e-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3115e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3115e-111">EXAMPLES</span></span>

### <span data-ttu-id="3115e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3115e-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="3115e-113">Desative a notificação.</span><span class="sxs-lookup"><span data-stu-id="3115e-113">Disable notification.</span></span>

### <span data-ttu-id="3115e-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3115e-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="3115e-115">Defina a notificação para o (s) endereço (s) de email personalizado e para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3115e-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="3115e-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3115e-116">Example 3</span></span>

<span data-ttu-id="3115e-117">Configurar as configurações de notificação do Azure site Recovery (notificação por email) para o cofre.</span><span class="sxs-lookup"><span data-stu-id="3115e-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="3115e-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="3115e-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="3115e-119">OS</span><span class="sxs-lookup"><span data-stu-id="3115e-119">PARAMETERS</span></span>

### <span data-ttu-id="3115e-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3115e-120">-CustomEmailAddress</span></span>
<span data-ttu-id="3115e-121">Alerta/notificação enviada para emails.</span><span class="sxs-lookup"><span data-stu-id="3115e-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="3115e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3115e-122">-DefaultProfile</span></span>
<span data-ttu-id="3115e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3115e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3115e-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3115e-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="3115e-125">Parâmetro switch especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3115e-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3115e-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="3115e-126">-DisableNotification</span></span>
<span data-ttu-id="3115e-127">Sinalizar para desabilitar todas as notificações.</span><span class="sxs-lookup"><span data-stu-id="3115e-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="3115e-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3115e-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="3115e-129">Parâmetro switch especifica habilitar notificação para o proprietário da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3115e-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3115e-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="3115e-130">-LocaleID</span></span>
<span data-ttu-id="3115e-131">Idioma de email do alerta/Notification para o usuário (códigos de cultura com suporte da Microsoft).</span><span class="sxs-lookup"><span data-stu-id="3115e-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="3115e-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3115e-132">-Confirm</span></span>
<span data-ttu-id="3115e-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3115e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3115e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3115e-134">-WhatIf</span></span>
<span data-ttu-id="3115e-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3115e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3115e-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3115e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3115e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3115e-137">CommonParameters</span></span>
<span data-ttu-id="3115e-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3115e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3115e-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3115e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3115e-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3115e-140">INPUTS</span></span>

### <span data-ttu-id="3115e-141">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3115e-141">None</span></span>

## <span data-ttu-id="3115e-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3115e-142">OUTPUTS</span></span>

### <span data-ttu-id="3115e-143">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3115e-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="3115e-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3115e-144">NOTES</span></span>

## <span data-ttu-id="3115e-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3115e-145">RELATED LINKS</span></span>
