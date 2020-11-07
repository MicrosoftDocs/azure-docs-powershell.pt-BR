---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: 194fcfddef0d85925bc08fb53fa7f5acf860e9ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777865"
---
# <span data-ttu-id="828cb-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="828cb-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="828cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="828cb-102">SYNOPSIS</span></span>
<span data-ttu-id="828cb-103">Obtém informações sobre a configuração de sincronização de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="828cb-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="828cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="828cb-104">SYNTAX</span></span>

### <span data-ttu-id="828cb-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="828cb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="828cb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="828cb-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="828cb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="828cb-107">DESCRIPTION</span></span>
<span data-ttu-id="828cb-108">O cmdlet **Get-AzDataShareSynchronization** fornece informações sobre todas as configurações de sincronização presentes em um compartilhamento em uma conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="828cb-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="828cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="828cb-109">EXAMPLES</span></span>

### <span data-ttu-id="828cb-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="828cb-110">Example 1</span></span>
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

<span data-ttu-id="828cb-111">Esses comandos fornecem informações sobre todas as configurações de sincronização presentes no share AdsShare no WikiAds de conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="828cb-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="828cb-112">OS</span><span class="sxs-lookup"><span data-stu-id="828cb-112">PARAMETERS</span></span>

### <span data-ttu-id="828cb-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="828cb-113">-AccountName</span></span>
<span data-ttu-id="828cb-114">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828cb-114">Azure data share account name</span></span>

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

### <span data-ttu-id="828cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="828cb-115">-DefaultProfile</span></span>
<span data-ttu-id="828cb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="828cb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="828cb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="828cb-117">-ResourceGroupName</span></span>
<span data-ttu-id="828cb-118">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="828cb-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="828cb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="828cb-119">-ResourceId</span></span>
<span data-ttu-id="828cb-120">ID do recurso de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828cb-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="828cb-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="828cb-121">-ShareName</span></span>
<span data-ttu-id="828cb-122">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="828cb-122">Azure data share name</span></span>

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

### <span data-ttu-id="828cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="828cb-123">CommonParameters</span></span>
<span data-ttu-id="828cb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="828cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="828cb-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="828cb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="828cb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="828cb-126">INPUTS</span></span>

### <span data-ttu-id="828cb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="828cb-127">System.String</span></span>

## <span data-ttu-id="828cb-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="828cb-128">OUTPUTS</span></span>

### <span data-ttu-id="828cb-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="828cb-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="828cb-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="828cb-130">NOTES</span></span>

## <span data-ttu-id="828cb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="828cb-131">RELATED LINKS</span></span>
