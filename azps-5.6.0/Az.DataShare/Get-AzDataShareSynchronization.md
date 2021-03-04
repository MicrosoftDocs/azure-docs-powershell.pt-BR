---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: a4d3adbcc63eda80bced31523a43cbbad4513205
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890279"
---
# <span data-ttu-id="137cf-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="137cf-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="137cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="137cf-102">SYNOPSIS</span></span>
<span data-ttu-id="137cf-103">Obtém informações sobre a configuração de sincronização para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="137cf-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="137cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="137cf-104">SYNTAX</span></span>

### <span data-ttu-id="137cf-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="137cf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="137cf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="137cf-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="137cf-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="137cf-107">DESCRIPTION</span></span>
<span data-ttu-id="137cf-108">O cmdlet **Get-AzDataShareSynchronization** fornece informações sobre toda a configuração de sincronização presente em um compartilhamento em uma conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="137cf-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="137cf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="137cf-109">EXAMPLES</span></span>

### <span data-ttu-id="137cf-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="137cf-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="137cf-111">Esses comandos fornece informações sobre todas as configurações de sincronização presentes no compartilhamento AdsShare na conta de compartilhamento de dados WikiAds.</span><span class="sxs-lookup"><span data-stu-id="137cf-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="137cf-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="137cf-112">PARAMETERS</span></span>

### <span data-ttu-id="137cf-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="137cf-113">-AccountName</span></span>
<span data-ttu-id="137cf-114">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="137cf-114">Azure data share account name</span></span>

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

### <span data-ttu-id="137cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137cf-115">-DefaultProfile</span></span>
<span data-ttu-id="137cf-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="137cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="137cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="137cf-118">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="137cf-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="137cf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="137cf-119">-ResourceId</span></span>
<span data-ttu-id="137cf-120">ID de recurso de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="137cf-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="137cf-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="137cf-121">-ShareName</span></span>
<span data-ttu-id="137cf-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="137cf-122">Azure data share name</span></span>

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

### <span data-ttu-id="137cf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137cf-123">CommonParameters</span></span>
<span data-ttu-id="137cf-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="137cf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137cf-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="137cf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137cf-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="137cf-126">INPUTS</span></span>

### <span data-ttu-id="137cf-127">System.String</span><span class="sxs-lookup"><span data-stu-id="137cf-127">System.String</span></span>

## <span data-ttu-id="137cf-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="137cf-128">OUTPUTS</span></span>

### <span data-ttu-id="137cf-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="137cf-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="137cf-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="137cf-130">NOTES</span></span>

## <span data-ttu-id="137cf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="137cf-131">RELATED LINKS</span></span>
