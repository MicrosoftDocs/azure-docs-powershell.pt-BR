---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesAccount.md
ms.openlocfilehash: 525483bdb99867ae9403c95a6bc2dc83a855704a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111709"
---
# <span data-ttu-id="8e24d-101">Update-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e24d-101">Update-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="8e24d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e24d-102">SYNOPSIS</span></span>
<span data-ttu-id="8e24d-103">Atualiza uma conta do Azure NetApp Files (ANF) de acordo com os modificadores opcionais fornecidos.</span><span class="sxs-lookup"><span data-stu-id="8e24d-103">Updates an Azure NetApp Files (ANF) account according to the optional modifiers provided.</span></span>

## <span data-ttu-id="8e24d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e24d-104">SYNTAX</span></span>

### <span data-ttu-id="8e24d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e24d-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e24d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e24d-106">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 -ResourceId <String> [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e24d-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e24d-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesAccount -ResourceGroupName <String> [-Location <String>] -Name <String>
 [-ActiveDirectory <PSNetAppFilesActiveDirectory[]>] -InputObject <PSNetAppFilesAccount> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e24d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e24d-108">DESCRIPTION</span></span>
<span data-ttu-id="8e24d-109">O **cmdlet Update-AzNetAppFilesAccount** modifica uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="8e24d-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF account.</span></span>

## <span data-ttu-id="8e24d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e24d-110">EXAMPLES</span></span>

### <span data-ttu-id="8e24d-111">Exemplo 1: atualiza uma conta ANF</span><span class="sxs-lookup"><span data-stu-id="8e24d-111">Example 1 : Updates an ANF account</span></span>
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

<span data-ttu-id="8e24d-112">Esse comando executa uma atualização na conta determinada modificando as marcas para as fornecidas.</span><span class="sxs-lookup"><span data-stu-id="8e24d-112">This command performs an update on the given account modifying the tags to those provided.</span></span>

## <span data-ttu-id="8e24d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e24d-113">PARAMETERS</span></span>

### <span data-ttu-id="8e24d-114">-ActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="8e24d-114">-ActiveDirectory</span></span>
<span data-ttu-id="8e24d-115">Uma matriz de tabela hash que representa os diretórios ativos</span><span class="sxs-lookup"><span data-stu-id="8e24d-115">A hashtable array which represents the active directories</span></span>

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

### <span data-ttu-id="8e24d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e24d-116">-DefaultProfile</span></span>
<span data-ttu-id="8e24d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e24d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e24d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e24d-118">-InputObject</span></span>
<span data-ttu-id="8e24d-119">O objeto da conta a ser atualizado</span><span class="sxs-lookup"><span data-stu-id="8e24d-119">The account object to update</span></span>

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

### <span data-ttu-id="8e24d-120">-Local</span><span class="sxs-lookup"><span data-stu-id="8e24d-120">-Location</span></span>
<span data-ttu-id="8e24d-121">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="8e24d-121">The location of the resource</span></span>

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

### <span data-ttu-id="8e24d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e24d-122">-Name</span></span>
<span data-ttu-id="8e24d-123">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8e24d-123">The name of the ANF account</span></span>

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

### <span data-ttu-id="8e24d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e24d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e24d-125">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8e24d-125">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8e24d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e24d-126">-ResourceId</span></span>
<span data-ttu-id="8e24d-127">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8e24d-127">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="8e24d-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e24d-128">-Tag</span></span>
<span data-ttu-id="8e24d-129">Uma tabela hash que representa marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="8e24d-129">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="8e24d-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8e24d-130">-Confirm</span></span>
<span data-ttu-id="8e24d-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e24d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e24d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e24d-132">-WhatIf</span></span>
<span data-ttu-id="8e24d-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8e24d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e24d-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e24d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e24d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e24d-135">CommonParameters</span></span>
<span data-ttu-id="8e24d-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e24d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e24d-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e24d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e24d-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="8e24d-138">INPUTS</span></span>

### <span data-ttu-id="8e24d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8e24d-139">System.String</span></span>

### <span data-ttu-id="8e24d-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e24d-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8e24d-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="8e24d-141">OUTPUTS</span></span>

### <span data-ttu-id="8e24d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8e24d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8e24d-143">Notas</span><span class="sxs-lookup"><span data-stu-id="8e24d-143">NOTES</span></span>

## <span data-ttu-id="8e24d-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e24d-144">RELATED LINKS</span></span>
