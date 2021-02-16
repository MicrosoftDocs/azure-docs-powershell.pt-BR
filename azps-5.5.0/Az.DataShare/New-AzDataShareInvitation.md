---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareInvitation.md
ms.openlocfilehash: ea042cb0db8fcb1995a935086d188efbb6c0647f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116414"
---
# <span data-ttu-id="01776-101">New-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="01776-101">New-AzDataShareInvitation</span></span>

## <span data-ttu-id="01776-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01776-102">SYNOPSIS</span></span>
<span data-ttu-id="01776-103">Cria um convite para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="01776-103">Creates an invitation for share.</span></span>

## <span data-ttu-id="01776-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01776-104">SYNTAX</span></span>

### <span data-ttu-id="01776-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="01776-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzDataShareInvitation [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01776-106">ByInvitationEmailParameterSet</span><span class="sxs-lookup"><span data-stu-id="01776-106">ByInvitationEmailParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetEmail <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01776-107">ByInvitationTenantParameterSet</span><span class="sxs-lookup"><span data-stu-id="01776-107">ByInvitationTenantParameterSet</span></span>
```
New-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 -TargetObjectId <String> -TargetTenantId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01776-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="01776-108">DESCRIPTION</span></span>
<span data-ttu-id="01776-109">O cmdlet **New-AzDataShareInvitation** envia um convite para o consumidor de destino com informações sobre o compartilhamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="01776-109">The **New-AzDataShareInvitation** cmdlet sends an invitation to the target consumer with information about the provider share.</span></span> 

## <span data-ttu-id="01776-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="01776-110">EXAMPLES</span></span>

### <span data-ttu-id="01776-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="01776-111">Example 1</span></span>
```
PS C:\> New-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation" -TargetEmail "adstest@microsoft.com"
InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/        providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="01776-112">Esse comando cria um convite AdsInvitation para compartilhar AdsShare e o envia para o email de adstest@microsoft.com destino.</span><span class="sxs-lookup"><span data-stu-id="01776-112">This command creates an invitation AdsInvitation for share AdsShare and sends it to target email adstest@microsoft.com.</span></span>

## <span data-ttu-id="01776-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01776-113">PARAMETERS</span></span>

### <span data-ttu-id="01776-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="01776-114">-AccountName</span></span>
<span data-ttu-id="01776-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="01776-115">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01776-116">-DefaultProfile</span></span>
<span data-ttu-id="01776-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01776-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01776-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="01776-118">-Name</span></span>
<span data-ttu-id="01776-119">Nome do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="01776-119">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01776-120">-ResourceGroupName</span></span>
<span data-ttu-id="01776-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="01776-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-122">-ShareName</span><span class="sxs-lookup"><span data-stu-id="01776-122">-ShareName</span></span>
<span data-ttu-id="01776-123">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="01776-123">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet, ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-124">-TargetEmail</span><span class="sxs-lookup"><span data-stu-id="01776-124">-TargetEmail</span></span>
<span data-ttu-id="01776-125">ID de email de destino</span><span class="sxs-lookup"><span data-stu-id="01776-125">Target email id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationEmailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-126">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="01776-126">-TargetObjectId</span></span>
<span data-ttu-id="01776-127">ID do objeto de destino</span><span class="sxs-lookup"><span data-stu-id="01776-127">Target object id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-128">-TargetTenantId</span><span class="sxs-lookup"><span data-stu-id="01776-128">-TargetTenantId</span></span>
<span data-ttu-id="01776-129">ID do locatário de destino</span><span class="sxs-lookup"><span data-stu-id="01776-129">Target tenant id</span></span>

```yaml
Type: System.String
Parameter Sets: ByInvitationTenantParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01776-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="01776-130">-Confirm</span></span>
<span data-ttu-id="01776-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01776-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01776-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01776-132">-WhatIf</span></span>
<span data-ttu-id="01776-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="01776-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01776-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01776-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01776-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01776-135">CommonParameters</span></span>
<span data-ttu-id="01776-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01776-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01776-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01776-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01776-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="01776-138">INPUTS</span></span>

### <span data-ttu-id="01776-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="01776-139">None</span></span>

## <span data-ttu-id="01776-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="01776-140">OUTPUTS</span></span>

### <span data-ttu-id="01776-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="01776-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="01776-142">Notas</span><span class="sxs-lookup"><span data-stu-id="01776-142">NOTES</span></span>

## <span data-ttu-id="01776-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01776-143">RELATED LINKS</span></span>
