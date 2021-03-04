---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 29846c8bb5650a667bf565fec273cbf24c8cd394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892184"
---
# <span data-ttu-id="e8999-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e8999-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="e8999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8999-102">SYNOPSIS</span></span>
<span data-ttu-id="e8999-103">Exclui uma conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8999-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e8999-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e8999-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8999-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e8999-105">DESCRIPTION</span></span>
<span data-ttu-id="e8999-106">O cmdlet **Remove-AzDataLakeAnalyticsAccount** exclui permanentemente uma conta do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8999-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e8999-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8999-107">EXAMPLES</span></span>

### <span data-ttu-id="e8999-108">Exemplo 1: Remover uma conta</span><span class="sxs-lookup"><span data-stu-id="e8999-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="e8999-109">Este comando remove a conta do Data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="e8999-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="e8999-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e8999-110">PARAMETERS</span></span>

### <span data-ttu-id="e8999-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8999-111">-DefaultProfile</span></span>
<span data-ttu-id="e8999-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e8999-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8999-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e8999-113">-Force</span></span>
<span data-ttu-id="e8999-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e8999-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e8999-115">-Name</span></span>
<span data-ttu-id="e8999-116">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8999-116">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8999-117">-PassThru</span></span>
<span data-ttu-id="e8999-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e8999-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8999-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e8999-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8999-120">-ResourceGroupName</span></span>
<span data-ttu-id="e8999-121">Especifica o nome do grupo de recursos da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e8999-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8999-122">-Confirm</span></span>
<span data-ttu-id="e8999-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8999-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8999-124">-WhatIf</span></span>
<span data-ttu-id="e8999-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e8999-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8999-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e8999-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8999-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8999-127">CommonParameters</span></span>
<span data-ttu-id="e8999-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8999-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8999-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8999-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8999-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8999-130">INPUTS</span></span>

### <span data-ttu-id="e8999-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e8999-131">System.String</span></span>

## <span data-ttu-id="e8999-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e8999-132">OUTPUTS</span></span>

### <span data-ttu-id="e8999-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e8999-133">System.Boolean</span></span>

## <span data-ttu-id="e8999-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="e8999-134">NOTES</span></span>

## <span data-ttu-id="e8999-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8999-135">RELATED LINKS</span></span>

[<span data-ttu-id="e8999-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e8999-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e8999-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e8999-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e8999-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e8999-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="e8999-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="e8999-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


