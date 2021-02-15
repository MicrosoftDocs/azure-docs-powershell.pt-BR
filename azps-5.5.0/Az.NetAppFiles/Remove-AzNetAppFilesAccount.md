---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f6e2421a20cb7aaf044d3abfbbddf7f5c72b37e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111719"
---
# <span data-ttu-id="52288-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="52288-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="52288-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52288-102">SYNOPSIS</span></span>
<span data-ttu-id="52288-103">Exclui uma conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="52288-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="52288-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52288-104">SYNTAX</span></span>

### <span data-ttu-id="52288-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="52288-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52288-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52288-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52288-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52288-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52288-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="52288-108">DESCRIPTION</span></span>
<span data-ttu-id="52288-109">O **cmdlet Remove-AzNetAppFilesAccount** exclui uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="52288-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="52288-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52288-110">EXAMPLES</span></span>

### <span data-ttu-id="52288-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="52288-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="52288-112">Esse comando exclui a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="52288-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="52288-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52288-113">PARAMETERS</span></span>

### <span data-ttu-id="52288-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52288-114">-DefaultProfile</span></span>
<span data-ttu-id="52288-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52288-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52288-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52288-116">-InputObject</span></span>
<span data-ttu-id="52288-117">O objeto da conta a ser removido</span><span class="sxs-lookup"><span data-stu-id="52288-117">The account object to remove</span></span>

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

### <span data-ttu-id="52288-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="52288-118">-Name</span></span>
<span data-ttu-id="52288-119">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="52288-119">The name of the ANF account</span></span>

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

### <span data-ttu-id="52288-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52288-120">-PassThru</span></span>
<span data-ttu-id="52288-121">Retornar se a conta especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="52288-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="52288-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52288-122">-ResourceGroupName</span></span>
<span data-ttu-id="52288-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="52288-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="52288-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52288-124">-ResourceId</span></span>
<span data-ttu-id="52288-125">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="52288-125">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="52288-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="52288-126">-Confirm</span></span>
<span data-ttu-id="52288-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52288-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52288-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52288-128">-WhatIf</span></span>
<span data-ttu-id="52288-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="52288-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52288-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52288-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52288-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52288-131">CommonParameters</span></span>
<span data-ttu-id="52288-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52288-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52288-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52288-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52288-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="52288-134">INPUTS</span></span>

### <span data-ttu-id="52288-135">System.String</span><span class="sxs-lookup"><span data-stu-id="52288-135">System.String</span></span>

### <span data-ttu-id="52288-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="52288-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="52288-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="52288-137">OUTPUTS</span></span>

### <span data-ttu-id="52288-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52288-138">System.Boolean</span></span>

## <span data-ttu-id="52288-139">Notas</span><span class="sxs-lookup"><span data-stu-id="52288-139">NOTES</span></span>

## <span data-ttu-id="52288-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52288-140">RELATED LINKS</span></span>
