---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110988"
---
# <span data-ttu-id="e3231-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e3231-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="e3231-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3231-102">SYNOPSIS</span></span>
<span data-ttu-id="e3231-103">Exclui permanentemente uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3231-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e3231-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3231-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3231-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3231-105">DESCRIPTION</span></span>
<span data-ttu-id="e3231-106">O cmdlet **Remove-AzDataLakeStoreAccount** exclui permanentemente uma conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3231-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="e3231-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3231-107">EXAMPLES</span></span>

### <span data-ttu-id="e3231-108">Exemplo 1: Remover uma conta do Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e3231-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="e3231-109">Esse comando remove a conta chamada ContosoADL da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e3231-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="e3231-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3231-110">PARAMETERS</span></span>

### <span data-ttu-id="e3231-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3231-111">-DefaultProfile</span></span>
<span data-ttu-id="e3231-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e3231-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3231-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e3231-113">-Force</span></span>
<span data-ttu-id="e3231-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3231-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3231-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3231-115">-Name</span></span>
<span data-ttu-id="e3231-116">Especifica o nome da conta a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e3231-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="e3231-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3231-117">-PassThru</span></span>
<span data-ttu-id="e3231-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e3231-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3231-119">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="e3231-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3231-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3231-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3231-121">Especifica o grupo de recursos que contém a conta a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e3231-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="e3231-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e3231-122">-Confirm</span></span>
<span data-ttu-id="e3231-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3231-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3231-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3231-124">-WhatIf</span></span>
<span data-ttu-id="e3231-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e3231-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3231-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3231-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3231-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3231-127">CommonParameters</span></span>
<span data-ttu-id="e3231-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3231-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3231-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3231-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3231-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3231-130">INPUTS</span></span>

### <span data-ttu-id="e3231-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e3231-131">System.String</span></span>

## <span data-ttu-id="e3231-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3231-132">OUTPUTS</span></span>

### <span data-ttu-id="e3231-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3231-133">System.Boolean</span></span>

## <span data-ttu-id="e3231-134">Notas</span><span class="sxs-lookup"><span data-stu-id="e3231-134">NOTES</span></span>

## <span data-ttu-id="e3231-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3231-135">RELATED LINKS</span></span>

[<span data-ttu-id="e3231-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e3231-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e3231-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e3231-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e3231-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e3231-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="e3231-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="e3231-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


