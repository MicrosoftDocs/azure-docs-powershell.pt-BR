---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareInvitation.md
ms.openlocfilehash: 0a723400bf92569a077abc64467c3cace56da0a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117717"
---
# <span data-ttu-id="f6e61-101">Get-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="f6e61-101">Get-AzDataShareInvitation</span></span>

## <span data-ttu-id="f6e61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6e61-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e61-103">Obtém convite de informações de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="f6e61-103">Gets information invitation of data share.</span></span>

## <span data-ttu-id="f6e61-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6e61-104">SYNTAX</span></span>

### <span data-ttu-id="f6e61-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6e61-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6e61-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e61-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareInvitation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6e61-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6e61-107">DESCRIPTION</span></span>
<span data-ttu-id="f6e61-108">O cmdlet **Get-AzDataShareInvitation** obtém informações sobre convites adicionados ao compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="f6e61-108">The **Get-AzDataShareInvitation** cmdlet gets information on invitations added in data share.</span></span> <span data-ttu-id="f6e61-109">Se você especificar o nome do convite, este cmdlet obterá informações sobre o convite.</span><span class="sxs-lookup"><span data-stu-id="f6e61-109">If you specify the name of the invitation, this cmdlet gets information about the invitation.</span></span> <span data-ttu-id="f6e61-110">Se você não especificar um nome, este cmdlet obterá informações sobre todos os convites em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f6e61-110">If you do not specify a name, this cmdlet gets information about all the invitations in a share.</span></span>

## <span data-ttu-id="f6e61-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6e61-111">EXAMPLES</span></span>

### <span data-ttu-id="f6e61-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6e61-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareInvitation -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsInvitation"

InvitationId     : 167e06ff-567f-4bc7-be0c-645a6de710f3
InvitationStatus : Pending
Sender           : adsprovider@microsoft.com
SentAt           : 7/8/2019 10:47:10 PM
TargetEmail      : adstest@microsoft.com
TargetObjectId   :
TargetTenantId   :
Id               : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/invitations/AdsInvitation
Name             : AdsInvitation
Type             : Microsoft.DataShare/Invitations
```

<span data-ttu-id="f6e61-113">Esses comandos fornece informações sobre convite AdsInvitation presentes no compartilhamento de dados AdsShare.</span><span class="sxs-lookup"><span data-stu-id="f6e61-113">This commands provides information about invitation AdsInvitation present in data share AdsShare.</span></span>

## <span data-ttu-id="f6e61-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6e61-114">PARAMETERS</span></span>

### <span data-ttu-id="f6e61-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f6e61-115">-AccountName</span></span>
<span data-ttu-id="f6e61-116">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f6e61-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e61-117">-DefaultProfile</span></span>
<span data-ttu-id="f6e61-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6e61-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e61-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6e61-119">-Name</span></span>
<span data-ttu-id="f6e61-120">Nome do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f6e61-120">Azure data share invitation name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e61-121">-ResourceGroupName</span></span>
<span data-ttu-id="f6e61-122">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="f6e61-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6e61-123">-ResourceId</span></span>
<span data-ttu-id="f6e61-124">A ID do recurso do convite de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f6e61-124">The resource id of the azure data share invitation</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f6e61-125">-ShareName</span></span>
<span data-ttu-id="f6e61-126">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f6e61-126">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6e61-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e61-127">CommonParameters</span></span>
<span data-ttu-id="f6e61-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6e61-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e61-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6e61-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e61-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6e61-130">INPUTS</span></span>

### <span data-ttu-id="f6e61-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f6e61-131">System.String</span></span>

## <span data-ttu-id="f6e61-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6e61-132">OUTPUTS</span></span>

### <span data-ttu-id="f6e61-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="f6e61-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="f6e61-134">Notas</span><span class="sxs-lookup"><span data-stu-id="f6e61-134">NOTES</span></span>

## <span data-ttu-id="f6e61-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6e61-135">RELATED LINKS</span></span>
