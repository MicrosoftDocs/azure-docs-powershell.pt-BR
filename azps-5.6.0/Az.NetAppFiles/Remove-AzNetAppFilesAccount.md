---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 19f194d9402c2d5101b1da56c7c7a2a2208345aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887434"
---
# <span data-ttu-id="8590e-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8590e-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="8590e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8590e-102">SYNOPSIS</span></span>
<span data-ttu-id="8590e-103">Exclui uma conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="8590e-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="8590e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8590e-104">SYNTAX</span></span>

### <span data-ttu-id="8590e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8590e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8590e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8590e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8590e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8590e-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8590e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8590e-108">DESCRIPTION</span></span>
<span data-ttu-id="8590e-109">O cmdlet **Remove-AzNetAppFilesAccount** exclui uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="8590e-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="8590e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8590e-110">EXAMPLES</span></span>

### <span data-ttu-id="8590e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8590e-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="8590e-112">Este comando exclui a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="8590e-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="8590e-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8590e-113">PARAMETERS</span></span>

### <span data-ttu-id="8590e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8590e-114">-DefaultProfile</span></span>
<span data-ttu-id="8590e-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8590e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8590e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8590e-116">-InputObject</span></span>
<span data-ttu-id="8590e-117">O objeto account a ser removido</span><span class="sxs-lookup"><span data-stu-id="8590e-117">The account object to remove</span></span>

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

### <span data-ttu-id="8590e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8590e-118">-Name</span></span>
<span data-ttu-id="8590e-119">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8590e-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8590e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8590e-120">-PassThru</span></span>
<span data-ttu-id="8590e-121">Retornar se a conta especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="8590e-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="8590e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8590e-122">-ResourceGroupName</span></span>
<span data-ttu-id="8590e-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8590e-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="8590e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8590e-124">-ResourceId</span></span>
<span data-ttu-id="8590e-125">A id de recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="8590e-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="8590e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8590e-126">-Confirm</span></span>
<span data-ttu-id="8590e-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8590e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8590e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8590e-128">-WhatIf</span></span>
<span data-ttu-id="8590e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8590e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8590e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8590e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8590e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8590e-131">CommonParameters</span></span>
<span data-ttu-id="8590e-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8590e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8590e-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8590e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8590e-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8590e-134">INPUTS</span></span>

### <span data-ttu-id="8590e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8590e-135">System.String</span></span>

### <span data-ttu-id="8590e-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="8590e-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="8590e-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8590e-137">OUTPUTS</span></span>

### <span data-ttu-id="8590e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8590e-138">System.Boolean</span></span>

## <span data-ttu-id="8590e-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="8590e-139">NOTES</span></span>

## <span data-ttu-id="8590e-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8590e-140">RELATED LINKS</span></span>
