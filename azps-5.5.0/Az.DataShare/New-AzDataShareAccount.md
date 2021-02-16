---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113241"
---
# <span data-ttu-id="597ca-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="597ca-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="597ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="597ca-102">SYNOPSIS</span></span>
<span data-ttu-id="597ca-103">Cria uma nova conta de compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="597ca-103">Creates new data share account</span></span>

## <span data-ttu-id="597ca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="597ca-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597ca-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="597ca-105">DESCRIPTION</span></span>
<span data-ttu-id="597ca-106">**O cmdlet New-AzDataShareAccount** cria uma conta de da ltda no grupo de recursos especificado do Azure.</span><span class="sxs-lookup"><span data-stu-id="597ca-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="597ca-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="597ca-107">EXAMPLES</span></span>

### <span data-ttu-id="597ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="597ca-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="597ca-109">Cria uma conta chamada "WikiADS" no grupo de recursos "ADS"</span><span class="sxs-lookup"><span data-stu-id="597ca-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="597ca-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="597ca-110">PARAMETERS</span></span>

### <span data-ttu-id="597ca-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="597ca-111">-AsJob</span></span>
<span data-ttu-id="597ca-112">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="597ca-112">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597ca-113">-DefaultProfile</span></span>
<span data-ttu-id="597ca-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="597ca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="597ca-115">-Local</span><span class="sxs-lookup"><span data-stu-id="597ca-115">-Location</span></span>
<span data-ttu-id="597ca-116">O local no qual criar a conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="597ca-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="597ca-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="597ca-117">-Name</span></span>
<span data-ttu-id="597ca-118">Nome da conta de compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="597ca-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="597ca-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597ca-119">-ResourceGroupName</span></span>
<span data-ttu-id="597ca-120">O nome do grupo de recursos da conta de compartilhamento de dados do azure será criado em.</span><span class="sxs-lookup"><span data-stu-id="597ca-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="597ca-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="597ca-121">-Tag</span></span>
<span data-ttu-id="597ca-122">As marcas a associar à conta de compartilhamento de dados do azure.</span><span class="sxs-lookup"><span data-stu-id="597ca-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597ca-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="597ca-123">-Confirm</span></span>
<span data-ttu-id="597ca-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597ca-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597ca-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597ca-125">-WhatIf</span></span>
<span data-ttu-id="597ca-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="597ca-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="597ca-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="597ca-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597ca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597ca-128">CommonParameters</span></span>
<span data-ttu-id="597ca-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597ca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597ca-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="597ca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597ca-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="597ca-131">INPUTS</span></span>

### <span data-ttu-id="597ca-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="597ca-132">None</span></span>

## <span data-ttu-id="597ca-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="597ca-133">OUTPUTS</span></span>

### <span data-ttu-id="597ca-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="597ca-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="597ca-135">Notas</span><span class="sxs-lookup"><span data-stu-id="597ca-135">NOTES</span></span>

## <span data-ttu-id="597ca-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="597ca-136">RELATED LINKS</span></span>
