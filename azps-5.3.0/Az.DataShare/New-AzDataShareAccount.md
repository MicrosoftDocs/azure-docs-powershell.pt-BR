---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271471"
---
# <span data-ttu-id="dfcaf-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="dfcaf-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="dfcaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dfcaf-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcaf-103">Cria uma nova conta de compartilhamento de dados</span><span class="sxs-lookup"><span data-stu-id="dfcaf-103">Creates new data share account</span></span>

## <span data-ttu-id="dfcaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dfcaf-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcaf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dfcaf-105">DESCRIPTION</span></span>
<span data-ttu-id="dfcaf-106">O cmdlet **New-AzDataShareAccount** cria uma conta de compartilhamento de DataShare no grupo de recursos do Azure especificado.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="dfcaf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfcaf-107">EXAMPLES</span></span>

### <span data-ttu-id="dfcaf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dfcaf-108">Example 1</span></span>
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

<span data-ttu-id="dfcaf-109">Cria uma conta chamada "WikiADS" no grupo de recursos "anúncios"</span><span class="sxs-lookup"><span data-stu-id="dfcaf-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="dfcaf-110">OS</span><span class="sxs-lookup"><span data-stu-id="dfcaf-110">PARAMETERS</span></span>

### <span data-ttu-id="dfcaf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfcaf-111">-AsJob</span></span>
<span data-ttu-id="dfcaf-112">{{Preencher Descrição AsJob}}</span><span class="sxs-lookup"><span data-stu-id="dfcaf-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="dfcaf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcaf-113">-DefaultProfile</span></span>
<span data-ttu-id="dfcaf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfcaf-115">-Local</span><span class="sxs-lookup"><span data-stu-id="dfcaf-115">-Location</span></span>
<span data-ttu-id="dfcaf-116">O local no qual criar a conta de compartilhamento de dados.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="dfcaf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfcaf-117">-Name</span></span>
<span data-ttu-id="dfcaf-118">Nome da conta do compartilhamento de dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="dfcaf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcaf-119">-ResourceGroupName</span></span>
<span data-ttu-id="dfcaf-120">O nome do grupo de recursos da conta do Azure data share será criado.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="dfcaf-121">-Marca</span><span class="sxs-lookup"><span data-stu-id="dfcaf-121">-Tag</span></span>
<span data-ttu-id="dfcaf-122">As marcas a serem associadas à conta do Azure data share.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="dfcaf-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dfcaf-123">-Confirm</span></span>
<span data-ttu-id="dfcaf-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfcaf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcaf-125">-WhatIf</span></span>
<span data-ttu-id="dfcaf-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfcaf-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfcaf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcaf-128">CommonParameters</span></span>
<span data-ttu-id="dfcaf-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcaf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcaf-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfcaf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcaf-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dfcaf-131">INPUTS</span></span>

### <span data-ttu-id="dfcaf-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="dfcaf-132">None</span></span>

## <span data-ttu-id="dfcaf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dfcaf-133">OUTPUTS</span></span>

### <span data-ttu-id="dfcaf-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="dfcaf-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="dfcaf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dfcaf-135">NOTES</span></span>

## <span data-ttu-id="dfcaf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfcaf-136">RELATED LINKS</span></span>
