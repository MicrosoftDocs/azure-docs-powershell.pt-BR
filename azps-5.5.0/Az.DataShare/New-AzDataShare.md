---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: 265f917068237fee13f77eb8c87e0adf8cd12f08
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113243"
---
# <span data-ttu-id="f9bb3-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="f9bb3-101">New-AzDataShare</span></span>

## <span data-ttu-id="f9bb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bb3-103">Cria um compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-103">Creates a azure data share.</span></span>

## <span data-ttu-id="f9bb3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9bb3-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9bb3-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="f9bb3-106">O cmdlet **New-AzDataShare** cria um compartilhamento de dados dentro de uma conta de compartilhamento de dados do Azure especificada, fornecendo o nome do grupo de recursos, o nome da conta, o nome do compartilhamento e o tipo de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="f9bb3-107">Descrição e termos de uso são parâmetros opcionais que podem ser definidos durante a criação do compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="f9bb3-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9bb3-108">EXAMPLES</span></span>

### <span data-ttu-id="f9bb3-109">Exemplo 1: Criar um compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="f9bb3-109">Example 1 : Create a data share</span></span>
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

<span data-ttu-id="f9bb3-110">Esse comando cria um compartilhamento de dados chamado AdsShare do tipo CopyBased na conta de compartilhamento de dados WikiAdsAccount sob ADS do grupo de recursos com descrição e termos de uso.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="f9bb3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9bb3-111">PARAMETERS</span></span>

### <span data-ttu-id="f9bb3-112">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="f9bb3-112">-AccountName</span></span>
<span data-ttu-id="f9bb3-113">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f9bb3-113">Azure data share account name</span></span>

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

### <span data-ttu-id="f9bb3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bb3-114">-DefaultProfile</span></span>
<span data-ttu-id="f9bb3-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9bb3-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="f9bb3-116">-Description</span></span>
<span data-ttu-id="f9bb3-117">Descrição do compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="f9bb3-117">Description of azure data share</span></span>

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

### <span data-ttu-id="f9bb3-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9bb3-118">-Name</span></span>
<span data-ttu-id="f9bb3-119">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f9bb3-119">Azure data share name</span></span>

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

### <span data-ttu-id="f9bb3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bb3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9bb3-121">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="f9bb3-121">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f9bb3-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="f9bb3-122">-TermsOfUse</span></span>
<span data-ttu-id="f9bb3-123">Termos de uso para o compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="f9bb3-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="f9bb3-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f9bb3-124">-Confirm</span></span>
<span data-ttu-id="f9bb3-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9bb3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9bb3-126">-WhatIf</span></span>
<span data-ttu-id="f9bb3-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9bb3-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9bb3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bb3-129">CommonParameters</span></span>
<span data-ttu-id="f9bb3-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9bb3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bb3-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9bb3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bb3-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9bb3-132">INPUTS</span></span>

### <span data-ttu-id="f9bb3-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f9bb3-133">None</span></span>

## <span data-ttu-id="f9bb3-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9bb3-134">OUTPUTS</span></span>

### <span data-ttu-id="f9bb3-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="f9bb3-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="f9bb3-136">Notas</span><span class="sxs-lookup"><span data-stu-id="f9bb3-136">NOTES</span></span>

## <span data-ttu-id="f9bb3-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9bb3-137">RELATED LINKS</span></span>
