---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 7fcf1f749816872fb7407fedaea10d06f3385441
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111713"
---
# <span data-ttu-id="1e4e1-101">Remove-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1e4e1-101">Remove-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1e4e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4e1-103">Exclui uma configuração do Azure NetApp Files (ANF) do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-103">Deletes an Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="1e4e1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e4e1-104">SYNTAX</span></span>

### <span data-ttu-id="1e4e1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1e4e1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e4e1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4e1-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> -AccountObject <PSNetAppFilesAccount>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4e1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4e1-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesActiveDirectory -InputObject <PSNetAppFilesActiveDirectory> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4e1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e4e1-108">DESCRIPTION</span></span>
<span data-ttu-id="1e4e1-109">O cmdlet **Remove-AzNetAppFilesActiveDirectory** exclui uma configuração do Active Directory ANF.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-109">The **Remove-AzNetAppFilesActiveDirectory** cmdlet deletes an ANF active directory configuration.</span></span>

## <span data-ttu-id="1e4e1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e4e1-110">EXAMPLES</span></span>

### <span data-ttu-id="1e4e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e4e1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName"
```

<span data-ttu-id="1e4e1-112">Esse comando exclui a nova configuração do Active Directory ANF com o nome "MyADName".</span><span class="sxs-lookup"><span data-stu-id="1e4e1-112">This command deletes the new ANF active directory configuration with a the name "MyADName".</span></span>

## <span data-ttu-id="1e4e1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e4e1-113">PARAMETERS</span></span>

### <span data-ttu-id="1e4e1-114">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="1e4e1-114">-AccountName</span></span>
<span data-ttu-id="1e4e1-115">O nome da conta da ANF</span><span class="sxs-lookup"><span data-stu-id="1e4e1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="1e4e1-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1e4e1-116">-AccountObject</span></span>
<span data-ttu-id="1e4e1-117">A Conta do objeto do Active Directory</span><span class="sxs-lookup"><span data-stu-id="1e4e1-117">The Account for the Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4e1-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="1e4e1-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="1e4e1-119">A ID do active directory ANF</span><span class="sxs-lookup"><span data-stu-id="1e4e1-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4e1-120">-DefaultProfile</span></span>
<span data-ttu-id="1e4e1-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4e1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e4e1-122">-InputObject</span></span>
<span data-ttu-id="1e4e1-123">O objeto do Active Directory a ser removido</span><span class="sxs-lookup"><span data-stu-id="1e4e1-123">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4e1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e4e1-124">-PassThru</span></span>
<span data-ttu-id="1e4e1-125">Retornar se o Active Directory especificado foi removido com êxito</span><span class="sxs-lookup"><span data-stu-id="1e4e1-125">Return whether the specified Active Directory  was successfully removed</span></span>

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

### <span data-ttu-id="1e4e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="1e4e1-127">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="1e4e1-127">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1e4e1-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1e4e1-128">-Confirm</span></span>
<span data-ttu-id="1e4e1-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4e1-130">-WhatIf</span></span>
<span data-ttu-id="1e4e1-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4e1-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4e1-133">CommonParameters</span></span>
<span data-ttu-id="1e4e1-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4e1-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e4e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4e1-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e4e1-136">INPUTS</span></span>

### <span data-ttu-id="1e4e1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="1e4e1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="1e4e1-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1e4e1-138">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1e4e1-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e4e1-139">OUTPUTS</span></span>

### <span data-ttu-id="1e4e1-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1e4e1-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1e4e1-141">Notas</span><span class="sxs-lookup"><span data-stu-id="1e4e1-141">NOTES</span></span>

## <span data-ttu-id="1e4e1-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e4e1-142">RELATED LINKS</span></span>
