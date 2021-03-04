---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: cda809b8c6c4425a3df7bd4ba5ae40a9292e358f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891429"
---
# <span data-ttu-id="73a53-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="73a53-101">New-AzDataShare</span></span>

## <span data-ttu-id="73a53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a53-102">SYNOPSIS</span></span>
<span data-ttu-id="73a53-103">Cria um compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="73a53-103">Creates a azure data share.</span></span>

## <span data-ttu-id="73a53-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73a53-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a53-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73a53-105">DESCRIPTION</span></span>
<span data-ttu-id="73a53-106">O cmdlet **New-AzDataShare** cria um compartilhamento de dados dentro de uma conta de compartilhamento de dados do azure especificada, fornecendo o nome do grupo de recursos, o nome da conta, o nome do compartilhamento e o tipo de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="73a53-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="73a53-107">Descrição e termos de uso são parâmetros opcionais que podem ser definidos durante a criação do compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="73a53-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="73a53-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73a53-108">EXAMPLES</span></span>

### <span data-ttu-id="73a53-109">Exemplo 1 : Criar um compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="73a53-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="73a53-110">Este comando cria um compartilhamento de dados chamado AdsShare do tipo CopyBased na conta de compartilhamento de dados WikiAdsAccount em ADS do grupo de recursos com descrição e termos de uso.</span><span class="sxs-lookup"><span data-stu-id="73a53-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="73a53-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73a53-111">PARAMETERS</span></span>

### <span data-ttu-id="73a53-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73a53-112">-AccountName</span></span>
<span data-ttu-id="73a53-113">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="73a53-113">Azure data share account name</span></span>

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

### <span data-ttu-id="73a53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a53-114">-DefaultProfile</span></span>
<span data-ttu-id="73a53-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73a53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73a53-116">-Description</span><span class="sxs-lookup"><span data-stu-id="73a53-116">-Description</span></span>
<span data-ttu-id="73a53-117">Descrição do compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="73a53-117">Description of azure data share</span></span>

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

### <span data-ttu-id="73a53-118">-Name</span><span class="sxs-lookup"><span data-stu-id="73a53-118">-Name</span></span>
<span data-ttu-id="73a53-119">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="73a53-119">Azure data share name</span></span>

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

### <span data-ttu-id="73a53-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a53-120">-ResourceGroupName</span></span>
<span data-ttu-id="73a53-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="73a53-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="73a53-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="73a53-122">-TermsOfUse</span></span>
<span data-ttu-id="73a53-123">Termos de uso para compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="73a53-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="73a53-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a53-124">-Confirm</span></span>
<span data-ttu-id="73a53-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73a53-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a53-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73a53-126">-WhatIf</span></span>
<span data-ttu-id="73a53-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73a53-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73a53-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73a53-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a53-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a53-129">CommonParameters</span></span>
<span data-ttu-id="73a53-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a53-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a53-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73a53-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a53-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73a53-132">INPUTS</span></span>

### <span data-ttu-id="73a53-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73a53-133">None</span></span>

## <span data-ttu-id="73a53-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73a53-134">OUTPUTS</span></span>

### <span data-ttu-id="73a53-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="73a53-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="73a53-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="73a53-136">NOTES</span></span>

## <span data-ttu-id="73a53-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73a53-137">RELATED LINKS</span></span>
