---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: c92348e32247bfed0b3aa7ce59b4772f7d3ef4af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944417"
---
# <span data-ttu-id="44912-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="44912-101">Set-AzDataShare</span></span>

## <span data-ttu-id="44912-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44912-102">SYNOPSIS</span></span>
<span data-ttu-id="44912-103">Atualiza um compartilhamento de dados existente</span><span class="sxs-lookup"><span data-stu-id="44912-103">Updates an existing data share</span></span>

## <span data-ttu-id="44912-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44912-104">SYNTAX</span></span>

### <span data-ttu-id="44912-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="44912-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44912-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44912-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44912-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44912-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44912-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44912-108">DESCRIPTION</span></span>
<span data-ttu-id="44912-109">O cmdlet **set-AzDataShare** atualiza um compartilhamento de dados que existe em uma conta do Azure data share especificada.</span><span class="sxs-lookup"><span data-stu-id="44912-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="44912-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44912-110">EXAMPLES</span></span>

### <span data-ttu-id="44912-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44912-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="44912-112">Este comando atualiza um compartilhamento de dados existente chamado AdsShare</span><span class="sxs-lookup"><span data-stu-id="44912-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="44912-113">OS</span><span class="sxs-lookup"><span data-stu-id="44912-113">PARAMETERS</span></span>

### <span data-ttu-id="44912-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44912-114">-AccountName</span></span>
<span data-ttu-id="44912-115">Nome da conta do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="44912-115">Azure data share account name</span></span>

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

### <span data-ttu-id="44912-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44912-116">-DefaultProfile</span></span>
<span data-ttu-id="44912-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44912-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44912-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="44912-118">-Description</span></span>
<span data-ttu-id="44912-119">Descrição do compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="44912-119">Description of Data Share</span></span>

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

### <span data-ttu-id="44912-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44912-120">-InputObject</span></span>
<span data-ttu-id="44912-121">Objeto de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="44912-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44912-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="44912-122">-Name</span></span>
<span data-ttu-id="44912-123">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="44912-123">Azure data share name</span></span>

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

### <span data-ttu-id="44912-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44912-124">-ResourceGroupName</span></span>
<span data-ttu-id="44912-125">O nome do grupo de recursos da conta do Azure data share</span><span class="sxs-lookup"><span data-stu-id="44912-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="44912-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44912-126">-ResourceId</span></span>
<span data-ttu-id="44912-127">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="44912-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="44912-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="44912-128">-TermsOfUse</span></span>
<span data-ttu-id="44912-129">Termos de uso do compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="44912-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="44912-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44912-130">-Confirm</span></span>
<span data-ttu-id="44912-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44912-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44912-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44912-132">-WhatIf</span></span>
<span data-ttu-id="44912-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44912-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44912-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44912-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44912-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44912-135">CommonParameters</span></span>
<span data-ttu-id="44912-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44912-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44912-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44912-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44912-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44912-138">INPUTS</span></span>

### <span data-ttu-id="44912-139">System. String</span><span class="sxs-lookup"><span data-stu-id="44912-139">System.String</span></span>

### <span data-ttu-id="44912-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="44912-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="44912-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44912-141">OUTPUTS</span></span>

### <span data-ttu-id="44912-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="44912-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="44912-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44912-143">NOTES</span></span>

## <span data-ttu-id="44912-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44912-144">RELATED LINKS</span></span>
