---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271486"
---
# <span data-ttu-id="2dec1-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="2dec1-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2dec1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2dec1-102">SYNOPSIS</span></span>
<span data-ttu-id="2dec1-103">Obtém informações sobre a configuração de sincronização em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2dec1-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="2dec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2dec1-104">SYNTAX</span></span>

### <span data-ttu-id="2dec1-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2dec1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dec1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dec1-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dec1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2dec1-107">DESCRIPTION</span></span>
<span data-ttu-id="2dec1-108">O cmdlet **Get-AzDataShareSynchronizationSetting** fornece informações sobre a sincronização habilitada em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="2dec1-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="2dec1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2dec1-109">EXAMPLES</span></span>

### <span data-ttu-id="2dec1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2dec1-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="2dec1-111">Este comando fornece informações sobre a sincronização ShareSynchronization habilitada no compartilhamento AdsShare em WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="2dec1-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="2dec1-112">OS</span><span class="sxs-lookup"><span data-stu-id="2dec1-112">PARAMETERS</span></span>

### <span data-ttu-id="2dec1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2dec1-113">-AccountName</span></span>
<span data-ttu-id="2dec1-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2dec1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="2dec1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dec1-115">-DefaultProfile</span></span>
<span data-ttu-id="2dec1-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2dec1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dec1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dec1-117">-Name</span></span>
<span data-ttu-id="2dec1-118">Nome para a configuração de sincronização</span><span class="sxs-lookup"><span data-stu-id="2dec1-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="2dec1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dec1-119">-ResourceGroupName</span></span>
<span data-ttu-id="2dec1-120">Nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="2dec1-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="2dec1-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2dec1-121">-ResourceId</span></span>
<span data-ttu-id="2dec1-122">A ID do recurso da configuração de sincronização do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2dec1-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="2dec1-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2dec1-123">-ShareName</span></span>
<span data-ttu-id="2dec1-124">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="2dec1-124">Azure data share name</span></span>

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

### <span data-ttu-id="2dec1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dec1-125">CommonParameters</span></span>
<span data-ttu-id="2dec1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dec1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dec1-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dec1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dec1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2dec1-128">INPUTS</span></span>

### <span data-ttu-id="2dec1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2dec1-129">System.String</span></span>

## <span data-ttu-id="2dec1-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2dec1-130">OUTPUTS</span></span>

### <span data-ttu-id="2dec1-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="2dec1-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="2dec1-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2dec1-132">NOTES</span></span>

## <span data-ttu-id="2dec1-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2dec1-133">RELATED LINKS</span></span>
