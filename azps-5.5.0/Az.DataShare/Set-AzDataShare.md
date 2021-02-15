---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: 69d44ea88b34aba027933cb3015a203bf06070fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115355"
---
# <span data-ttu-id="9397e-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="9397e-101">Set-AzDataShare</span></span>

## <span data-ttu-id="9397e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9397e-102">SYNOPSIS</span></span>
<span data-ttu-id="9397e-103">Atualiza um compartilhamento de dados existente</span><span class="sxs-lookup"><span data-stu-id="9397e-103">Updates an existing data share</span></span>

## <span data-ttu-id="9397e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9397e-104">SYNTAX</span></span>

### <span data-ttu-id="9397e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9397e-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9397e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9397e-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9397e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9397e-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9397e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9397e-108">DESCRIPTION</span></span>
<span data-ttu-id="9397e-109">O **cmdlet Set-AzDataShare** atualiza um compartilhamento de dados que existe dentro de uma conta de compartilhamento de dados do azure especificada.</span><span class="sxs-lookup"><span data-stu-id="9397e-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="9397e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9397e-110">EXAMPLES</span></span>

### <span data-ttu-id="9397e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9397e-111">Example 1</span></span>
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

<span data-ttu-id="9397e-112">Este comando atualiza um compartilhamento de dados existente chamado AdsShare</span><span class="sxs-lookup"><span data-stu-id="9397e-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="9397e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9397e-113">PARAMETERS</span></span>

### <span data-ttu-id="9397e-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="9397e-114">-AccountName</span></span>
<span data-ttu-id="9397e-115">Nome da conta de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="9397e-115">Azure data share account name</span></span>

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

### <span data-ttu-id="9397e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9397e-116">-DefaultProfile</span></span>
<span data-ttu-id="9397e-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9397e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9397e-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="9397e-118">-Description</span></span>
<span data-ttu-id="9397e-119">Descrição do Compartilhamento de Dados</span><span class="sxs-lookup"><span data-stu-id="9397e-119">Description of Data Share</span></span>

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

### <span data-ttu-id="9397e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9397e-120">-InputObject</span></span>
<span data-ttu-id="9397e-121">Objeto de compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="9397e-121">Azure data share object</span></span>


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

### <span data-ttu-id="9397e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9397e-122">-Name</span></span>
<span data-ttu-id="9397e-123">Nome do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="9397e-123">Azure data share name</span></span>

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

### <span data-ttu-id="9397e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9397e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9397e-125">O nome do grupo de recursos da conta de compartilhamento de dados do azure</span><span class="sxs-lookup"><span data-stu-id="9397e-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9397e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9397e-126">-ResourceId</span></span>
<span data-ttu-id="9397e-127">A ID do recurso do compartilhamento de dados do Azure</span><span class="sxs-lookup"><span data-stu-id="9397e-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="9397e-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="9397e-128">-TermsOfUse</span></span>
<span data-ttu-id="9397e-129">Termos de Uso para Compartilhamento de Dados</span><span class="sxs-lookup"><span data-stu-id="9397e-129">Terms of Use for Data Share</span></span>

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

### <span data-ttu-id="9397e-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9397e-130">-Confirm</span></span>
<span data-ttu-id="9397e-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9397e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9397e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9397e-132">-WhatIf</span></span>
<span data-ttu-id="9397e-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9397e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9397e-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9397e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9397e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9397e-135">CommonParameters</span></span>
<span data-ttu-id="9397e-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9397e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9397e-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9397e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9397e-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="9397e-138">INPUTS</span></span>

### <span data-ttu-id="9397e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9397e-139">System.String</span></span>

### <span data-ttu-id="9397e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="9397e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="9397e-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="9397e-141">OUTPUTS</span></span>

### <span data-ttu-id="9397e-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="9397e-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="9397e-143">Notas</span><span class="sxs-lookup"><span data-stu-id="9397e-143">NOTES</span></span>

## <span data-ttu-id="9397e-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9397e-144">RELATED LINKS</span></span>
