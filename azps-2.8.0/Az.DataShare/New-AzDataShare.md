---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: ccb40de9ef5e9e68cf62b7b05edeaac9ae10efbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596716"
---
# <span data-ttu-id="d2924-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="d2924-101">New-AzDataShare</span></span>

## <span data-ttu-id="d2924-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2924-102">SYNOPSIS</span></span>
<span data-ttu-id="d2924-103">Cria um compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2924-103">Creates a azure data share.</span></span>

## <span data-ttu-id="d2924-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2924-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2924-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2924-105">DESCRIPTION</span></span>
<span data-ttu-id="d2924-106">O cmdlet **New-AzDataShare** cria um compartilhamento de dados em uma conta especificada do Azure data share fornecendo o nome do grupo de recursos, o nome da conta, o nome do compartilhamento e o tipo de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d2924-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="d2924-107">A descrição e os termos de uso são parâmetros opcionais que podem ser definidos durante a criação do compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="d2924-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="d2924-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2924-108">EXAMPLES</span></span>

### <span data-ttu-id="d2924-109">Exemplo 1: criar um compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="d2924-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
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

<span data-ttu-id="d2924-110">Esse comando cria um compartilhamento de dados denominado AdsShare do tipo CopyBased na conta de compartilhamento de dados WikiAdsAccount em anúncios de grupo de recursos com descrição e termos de uso.</span><span class="sxs-lookup"><span data-stu-id="d2924-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="d2924-111">OS</span><span class="sxs-lookup"><span data-stu-id="d2924-111">PARAMETERS</span></span>

### <span data-ttu-id="d2924-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d2924-112">-AccountName</span></span>
<span data-ttu-id="d2924-113">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d2924-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2924-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2924-114">-DefaultProfile</span></span>
<span data-ttu-id="d2924-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2924-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2924-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="d2924-116">-Description</span></span>
<span data-ttu-id="d2924-117">Descrição do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d2924-117">Description of azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2924-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2924-118">-Name</span></span>
<span data-ttu-id="d2924-119">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="d2924-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2924-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2924-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2924-121">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d2924-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2924-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="d2924-122">-TermsOfUse</span></span>
<span data-ttu-id="d2924-123">Termos de uso do Azure data share</span><span class="sxs-lookup"><span data-stu-id="d2924-123">Terms of use for azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2924-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2924-124">-Confirm</span></span>
<span data-ttu-id="d2924-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2924-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2924-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2924-126">-WhatIf</span></span>
<span data-ttu-id="d2924-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2924-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2924-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2924-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2924-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2924-129">CommonParameters</span></span>
<span data-ttu-id="d2924-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2924-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2924-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2924-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2924-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2924-132">INPUTS</span></span>

### <span data-ttu-id="d2924-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d2924-133">None</span></span>

## <span data-ttu-id="d2924-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2924-134">OUTPUTS</span></span>

### <span data-ttu-id="d2924-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="d2924-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="d2924-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2924-136">NOTES</span></span>

## <span data-ttu-id="d2924-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2924-137">RELATED LINKS</span></span>
