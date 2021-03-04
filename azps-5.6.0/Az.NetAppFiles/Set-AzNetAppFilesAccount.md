---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/set-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Set-AzNetAppFilesAccount.md
ms.openlocfilehash: c5b8059561b859bd4ea7698b2cb41c9eb9a50a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887413"
---
# <span data-ttu-id="73c8b-101">Set-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="73c8b-101">Set-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="73c8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73c8b-102">SYNOPSIS</span></span>
<span data-ttu-id="73c8b-103">Atualiza uma conta do Azure NetApp Files (ANF) com o novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="73c8b-103">Updates an Azure NetApp Files (ANF) account with the new data set.</span></span> <span data-ttu-id="73c8b-104">Útil para excluir diretórios ativos associados.</span><span class="sxs-lookup"><span data-stu-id="73c8b-104">Useful for deletion of associated active directories.</span></span>

## <span data-ttu-id="73c8b-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="73c8b-105">SYNTAX</span></span>

### <span data-ttu-id="73c8b-106">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="73c8b-106">ByFieldsParameterSet (Default)</span></span>
```
Set-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> -Name <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73c8b-107">SetByResourceActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="73c8b-107">SetByResourceActiveDirectory</span></span>
```
Set-AzNetAppFilesAccount -Location <String> -Name <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73c8b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="73c8b-108">DESCRIPTION</span></span>
<span data-ttu-id="73c8b-109">O cmdlet **Set-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="73c8b-109">The **Set-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="73c8b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="73c8b-110">EXAMPLES</span></span>

### <span data-ttu-id="73c8b-111">Exemplo 1 : Modificar uma conta ANF</span><span class="sxs-lookup"><span data-stu-id="73c8b-111">Example 1 : Modify an ANF account</span></span>
```
PS C:\>Set-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="73c8b-112">Este comando executa uma atualização na conta determinada.</span><span class="sxs-lookup"><span data-stu-id="73c8b-112">This command performs an update on the given account.</span></span> <span data-ttu-id="73c8b-113">A ausência do active directory significa que ele será removido da conta.</span><span class="sxs-lookup"><span data-stu-id="73c8b-113">The absence of the active directory means it will be removed from the account.</span></span>

## <span data-ttu-id="73c8b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="73c8b-114">PARAMETERS</span></span>

### <span data-ttu-id="73c8b-115">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="73c8b-115">-ActiveDirectory</span></span>
<span data-ttu-id="73c8b-116">Uma matriz hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="73c8b-116">A hashtable array which represents the active directories</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory[]
Parameter Sets: SetByResourceActiveDirectory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73c8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73c8b-117">-DefaultProfile</span></span>
<span data-ttu-id="73c8b-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="73c8b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73c8b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="73c8b-119">-Location</span></span>
<span data-ttu-id="73c8b-120">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="73c8b-120">The location of the resource</span></span>

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

### <span data-ttu-id="73c8b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73c8b-121">-Name</span></span>
<span data-ttu-id="73c8b-122">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="73c8b-122">The name of the ANF account</span></span>

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

### <span data-ttu-id="73c8b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73c8b-123">-ResourceGroupName</span></span>
<span data-ttu-id="73c8b-124">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="73c8b-124">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="73c8b-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="73c8b-125">-Tag</span></span>
<span data-ttu-id="73c8b-126">Uma hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="73c8b-126">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="73c8b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73c8b-127">-Confirm</span></span>
<span data-ttu-id="73c8b-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73c8b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73c8b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73c8b-129">-WhatIf</span></span>
<span data-ttu-id="73c8b-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="73c8b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73c8b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="73c8b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73c8b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73c8b-132">CommonParameters</span></span>
<span data-ttu-id="73c8b-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73c8b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73c8b-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73c8b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73c8b-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73c8b-135">INPUTS</span></span>

### <span data-ttu-id="73c8b-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="73c8b-136">None</span></span>

## <span data-ttu-id="73c8b-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="73c8b-137">OUTPUTS</span></span>

### <span data-ttu-id="73c8b-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="73c8b-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="73c8b-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="73c8b-139">NOTES</span></span>

## <span data-ttu-id="73c8b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="73c8b-140">RELATED LINKS</span></span>
