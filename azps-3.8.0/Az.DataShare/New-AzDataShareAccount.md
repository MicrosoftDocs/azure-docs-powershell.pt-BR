---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 2b3eda3aadca93415d93154a9a70361c789c94ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777444"
---
# <span data-ttu-id="45dfc-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="45dfc-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="45dfc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="45dfc-103">Cria uma nova conta de compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="45dfc-103">Creates new data share account</span></span>

## <span data-ttu-id="45dfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45dfc-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45dfc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45dfc-105">DESCRIPTION</span></span>
<span data-ttu-id="45dfc-106">O cmdlet **New-AzDataShareAccount** cria uma conta de compartilhamento de DataShare no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="45dfc-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="45dfc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45dfc-107">EXAMPLES</span></span>

### <span data-ttu-id="45dfc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45dfc-108">Example 1</span></span>
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

<span data-ttu-id="45dfc-109">Cria uma conta chamada "WikiADS" no grupo de recursos "anúncios"</span><span class="sxs-lookup"><span data-stu-id="45dfc-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="45dfc-110">OS</span><span class="sxs-lookup"><span data-stu-id="45dfc-110">PARAMETERS</span></span>

### <span data-ttu-id="45dfc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45dfc-111">-AsJob</span></span>
<span data-ttu-id="45dfc-112">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="45dfc-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="45dfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45dfc-113">-DefaultProfile</span></span>
<span data-ttu-id="45dfc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45dfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45dfc-115">-Local</span><span class="sxs-lookup"><span data-stu-id="45dfc-115">-Location</span></span>
<span data-ttu-id="45dfc-116">O local no qual criar a conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="45dfc-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="45dfc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="45dfc-117">-Name</span></span>
<span data-ttu-id="45dfc-118">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="45dfc-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="45dfc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45dfc-119">-ResourceGroupName</span></span>
<span data-ttu-id="45dfc-120">O nome do grupo de recursos da conta do Azure data share será criado.</span><span class="sxs-lookup"><span data-stu-id="45dfc-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="45dfc-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="45dfc-121">-Tag</span></span>
<span data-ttu-id="45dfc-122">As marcas a serem associadas à conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="45dfc-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="45dfc-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45dfc-123">-Confirm</span></span>
<span data-ttu-id="45dfc-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45dfc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45dfc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45dfc-125">-WhatIf</span></span>
<span data-ttu-id="45dfc-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45dfc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45dfc-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45dfc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45dfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45dfc-128">CommonParameters</span></span>
<span data-ttu-id="45dfc-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45dfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45dfc-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45dfc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45dfc-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45dfc-131">INPUTS</span></span>

### <span data-ttu-id="45dfc-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="45dfc-132">None</span></span>

## <span data-ttu-id="45dfc-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45dfc-133">OUTPUTS</span></span>

### <span data-ttu-id="45dfc-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="45dfc-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="45dfc-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45dfc-135">NOTES</span></span>

## <span data-ttu-id="45dfc-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45dfc-136">RELATED LINKS</span></span>
