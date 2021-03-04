---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 2a31b5af374b1bc0f6136da61aa1c3672274e913
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887404"
---
# <span data-ttu-id="901ba-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="901ba-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="901ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="901ba-102">SYNOPSIS</span></span>
<span data-ttu-id="901ba-103">Atualiza uma conta do Azure NetApp Files (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="901ba-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="901ba-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="901ba-104">SYNTAX</span></span>

### <span data-ttu-id="901ba-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="901ba-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="901ba-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="901ba-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="901ba-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="901ba-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="901ba-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="901ba-108">DESCRIPTION</span></span>
<span data-ttu-id="901ba-109">O cmdlet **Update-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="901ba-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="901ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="901ba-110">EXAMPLES</span></span>

### <span data-ttu-id="901ba-111">Exemplo 1 : atualiza uma conta ANF</span><span class="sxs-lookup"><span data-stu-id="901ba-111">Example 1 : Updates an ANF account</span></span>
```
PS C:\>Update-AzNetAppFilesAccount -ResourceGroupName "MyRG" -l "westus2" -Name "MyAnfAccount" -Tag @{'Tag1' = 'Value1'}

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              : {Tag1}
AccountId         : 9fa2ca6d-1e48-4439-30e3-7de056e44e5a
ActiveDirectories :
ProvisioningState : Succeeded
```

<span data-ttu-id="901ba-112">Este comando executa uma atualização na conta fornecida modificando as marcas para as fornecidas.</span><span class="sxs-lookup"><span data-stu-id="901ba-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="901ba-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="901ba-113">PARAMETERS</span></span>

### <span data-ttu-id="901ba-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="901ba-114">-ActiveDirectory</span></span>
<span data-ttu-id="901ba-115">Uma matriz hashtable que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="901ba-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="901ba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901ba-116">-DefaultProfile</span></span>
<span data-ttu-id="901ba-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="901ba-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="901ba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="901ba-118">-InputObject</span></span>
<span data-ttu-id="901ba-119">O objeto account a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="901ba-119">The account object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="901ba-120">-Location</span><span class="sxs-lookup"><span data-stu-id="901ba-120">-Location</span></span>
<span data-ttu-id="901ba-121">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="901ba-121">The location of the resource</span></span>

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

### <span data-ttu-id="901ba-122">-Name</span><span class="sxs-lookup"><span data-stu-id="901ba-122">-Name</span></span>
<span data-ttu-id="901ba-123">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="901ba-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="901ba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901ba-124">-ResourceGroupName</span></span>
<span data-ttu-id="901ba-125">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="901ba-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="901ba-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="901ba-126">-ResourceId</span></span>
<span data-ttu-id="901ba-127">A id de recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="901ba-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="901ba-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="901ba-128">-Tag</span></span>
<span data-ttu-id="901ba-129">Uma hashtable que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="901ba-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="901ba-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="901ba-130">-Confirm</span></span>
<span data-ttu-id="901ba-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="901ba-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="901ba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="901ba-132">-WhatIf</span></span>
<span data-ttu-id="901ba-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="901ba-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="901ba-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="901ba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="901ba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901ba-135">CommonParameters</span></span>
<span data-ttu-id="901ba-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="901ba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901ba-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="901ba-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901ba-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="901ba-138">INPUTS</span></span>

### <span data-ttu-id="901ba-139">System.String</span><span class="sxs-lookup"><span data-stu-id="901ba-139">System.String</span></span>

### <span data-ttu-id="901ba-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="901ba-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="901ba-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="901ba-141">OUTPUTS</span></span>

### <span data-ttu-id="901ba-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="901ba-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="901ba-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="901ba-143">NOTES</span></span>

## <span data-ttu-id="901ba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="901ba-144">RELATED LINKS</span></span>
