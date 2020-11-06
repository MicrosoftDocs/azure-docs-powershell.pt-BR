---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596906"
---
# <span data-ttu-id="603f0-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="603f0-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="603f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="603f0-102">SYNOPSIS</span></span>
<span data-ttu-id="603f0-103">Exclui uma conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="603f0-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="603f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="603f0-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="603f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="603f0-105">DESCRIPTION</span></span>
<span data-ttu-id="603f0-106">O cmdlet **Remove-AzDataLakeAnalyticsAccount** exclui permanentemente uma conta do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="603f0-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="603f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="603f0-107">EXAMPLES</span></span>

### <span data-ttu-id="603f0-108">Exemplo 1: remover uma conta</span><span class="sxs-lookup"><span data-stu-id="603f0-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="603f0-109">Este comando Remove a conta do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="603f0-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="603f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="603f0-110">PARAMETERS</span></span>

### <span data-ttu-id="603f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="603f0-111">-DefaultProfile</span></span>
<span data-ttu-id="603f0-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="603f0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="603f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="603f0-113">-Force</span></span>
<span data-ttu-id="603f0-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="603f0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="603f0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="603f0-115">-Name</span></span>
<span data-ttu-id="603f0-116">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="603f0-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="603f0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="603f0-117">-PassThru</span></span>
<span data-ttu-id="603f0-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="603f0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="603f0-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="603f0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="603f0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="603f0-120">-ResourceGroupName</span></span>
<span data-ttu-id="603f0-121">Especifica o nome do grupo de recursos da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="603f0-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="603f0-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="603f0-122">-Confirm</span></span>
<span data-ttu-id="603f0-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="603f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="603f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="603f0-124">-WhatIf</span></span>
<span data-ttu-id="603f0-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="603f0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="603f0-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="603f0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="603f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603f0-127">CommonParameters</span></span>
<span data-ttu-id="603f0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="603f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603f0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="603f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603f0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="603f0-130">INPUTS</span></span>

### <span data-ttu-id="603f0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="603f0-131">System.String</span></span>

## <span data-ttu-id="603f0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="603f0-132">OUTPUTS</span></span>

### <span data-ttu-id="603f0-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="603f0-133">System.Boolean</span></span>

## <span data-ttu-id="603f0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="603f0-134">NOTES</span></span>

## <span data-ttu-id="603f0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="603f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="603f0-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="603f0-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="603f0-137">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="603f0-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="603f0-138">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="603f0-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="603f0-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="603f0-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


