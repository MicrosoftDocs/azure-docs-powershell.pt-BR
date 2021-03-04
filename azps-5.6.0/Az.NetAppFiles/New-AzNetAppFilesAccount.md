---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 588952f9f3aa0cb9c7351ee862ad6db82d66f85d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887448"
---
# <span data-ttu-id="e47d5-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e47d5-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="e47d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e47d5-103">Cria uma nova conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="e47d5-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="e47d5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e47d5-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e47d5-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e47d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e47d5-106">O cmdlet **New-AzNetAppFilesAccount** cria uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="e47d5-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="e47d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e47d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e47d5-108">Exemplo 1: Criar uma conta ANF</span><span class="sxs-lookup"><span data-stu-id="e47d5-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="e47d5-109">Este comando cria a nova conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e47d5-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="e47d5-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e47d5-110">PARAMETERS</span></span>

### <span data-ttu-id="e47d5-111">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="e47d5-111">-ActiveDirectory</span></span>
<span data-ttu-id="e47d5-112">Uma matriz hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="e47d5-112">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47d5-113">-DefaultProfile</span></span>
<span data-ttu-id="e47d5-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e47d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e47d5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="e47d5-115">-Location</span></span>
<span data-ttu-id="e47d5-116">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="e47d5-116">The location of the resource</span></span>

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

### <span data-ttu-id="e47d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e47d5-117">-Name</span></span>
<span data-ttu-id="e47d5-118">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e47d5-118">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e47d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="e47d5-120">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="e47d5-120">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="e47d5-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="e47d5-121">-Tag</span></span>
<span data-ttu-id="e47d5-122">Uma hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="e47d5-122">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47d5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e47d5-123">-Confirm</span></span>
<span data-ttu-id="e47d5-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e47d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e47d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e47d5-125">-WhatIf</span></span>
<span data-ttu-id="e47d5-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e47d5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e47d5-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e47d5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e47d5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47d5-128">CommonParameters</span></span>
<span data-ttu-id="e47d5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47d5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47d5-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e47d5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47d5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e47d5-131">INPUTS</span></span>

### <span data-ttu-id="e47d5-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e47d5-132">None</span></span>

## <span data-ttu-id="e47d5-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e47d5-133">OUTPUTS</span></span>

### <span data-ttu-id="e47d5-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e47d5-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e47d5-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="e47d5-135">NOTES</span></span>

## <span data-ttu-id="e47d5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e47d5-136">RELATED LINKS</span></span>
