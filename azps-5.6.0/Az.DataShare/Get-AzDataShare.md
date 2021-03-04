---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: 1cccba1d3af4bcd1ff69ad04f248615e1edb66fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891385"
---
# <span data-ttu-id="242ce-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="242ce-101">Get-AzDataShare</span></span>

## <span data-ttu-id="242ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="242ce-102">SYNOPSIS</span></span>
<span data-ttu-id="242ce-103">Obter informações sobre Compartilhamentos de Dados.</span><span class="sxs-lookup"><span data-stu-id="242ce-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="242ce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="242ce-104">SYNTAX</span></span>

### <span data-ttu-id="242ce-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="242ce-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="242ce-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="242ce-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="242ce-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="242ce-107">DESCRIPTION</span></span>
<span data-ttu-id="242ce-108">O cmdlet **Get-AzDataShare** obtém informações sobre compartilhamentos de dados em um accoount de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="242ce-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="242ce-109">Se você especificar o nome de um compartilhamento de dados, esse cmdlet obterá informações sobre esse compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="242ce-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="242ce-110">Se você não especificar um nome, este cmdlet obterá informações sobre todos os compartilhamentos de dados em uma conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="242ce-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="242ce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="242ce-111">EXAMPLES</span></span>

### <span data-ttu-id="242ce-112">Exemplo 1 : Obter um compartilhamento de dados específico</span><span class="sxs-lookup"><span data-stu-id="242ce-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="242ce-113">Este comando exibe informações sobre compartilhamento de dados AdsShare na conta de compartilhamento de dados do Azure WikiAdsAccount e ADS do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="242ce-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="242ce-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="242ce-114">PARAMETERS</span></span>

### <span data-ttu-id="242ce-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="242ce-115">-AccountName</span></span>
<span data-ttu-id="242ce-116">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="242ce-116">Azure data share account name</span></span>

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

### <span data-ttu-id="242ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="242ce-117">-DefaultProfile</span></span>
<span data-ttu-id="242ce-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="242ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="242ce-119">-Name</span><span class="sxs-lookup"><span data-stu-id="242ce-119">-Name</span></span>
<span data-ttu-id="242ce-120">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="242ce-120">Azure data share name</span></span>

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

### <span data-ttu-id="242ce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="242ce-121">-ResourceGroupName</span></span>
<span data-ttu-id="242ce-122">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="242ce-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="242ce-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="242ce-123">-ResourceId</span></span>
<span data-ttu-id="242ce-124">A id de recurso do compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="242ce-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="242ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="242ce-125">CommonParameters</span></span>
<span data-ttu-id="242ce-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="242ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="242ce-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="242ce-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="242ce-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="242ce-128">INPUTS</span></span>

### <span data-ttu-id="242ce-129">System.String</span><span class="sxs-lookup"><span data-stu-id="242ce-129">System.String</span></span>

## <span data-ttu-id="242ce-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="242ce-130">OUTPUTS</span></span>

### <span data-ttu-id="242ce-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="242ce-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="242ce-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="242ce-132">NOTES</span></span>

## <span data-ttu-id="242ce-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="242ce-133">RELATED LINKS</span></span>
