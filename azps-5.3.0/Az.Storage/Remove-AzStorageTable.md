---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432934"
---
# <span data-ttu-id="4ddb7-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ddb7-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="4ddb7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ddb7-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddb7-103">Remove uma tabela de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-103">Removes a storage table.</span></span>

## <span data-ttu-id="4ddb7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ddb7-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ddb7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ddb7-105">DESCRIPTION</span></span>
<span data-ttu-id="4ddb7-106">O cmdlet **Remove-AzStorageTable** remove uma ou mais tabelas de armazenamento de uma conta de armazenamento no Azure.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="4ddb7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ddb7-107">EXAMPLES</span></span>

### <span data-ttu-id="4ddb7-108">Exemplo 1: remover uma tabela</span><span class="sxs-lookup"><span data-stu-id="4ddb7-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="4ddb7-109">Esse comando Remove uma tabela.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-109">This command removes a table.</span></span>

### <span data-ttu-id="4ddb7-110">Exemplo 2: remover várias tabelas</span><span class="sxs-lookup"><span data-stu-id="4ddb7-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="4ddb7-111">Este exemplo usa um caractere curinga com o parâmetro *Name* para obter todas as tabelas correspondentes à tabela padrão e, em seguida, passa o resultado no pipeline para remover as tabelas.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="4ddb7-112">OS</span><span class="sxs-lookup"><span data-stu-id="4ddb7-112">PARAMETERS</span></span>

### <span data-ttu-id="4ddb7-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="4ddb7-113">-Context</span></span>
<span data-ttu-id="4ddb7-114">Especifica o contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4ddb7-115">Você pode criá-lo usando o cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddb7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ddb7-116">-DefaultProfile</span></span>
<span data-ttu-id="4ddb7-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ddb7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4ddb7-118">-Force</span></span>
<span data-ttu-id="4ddb7-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ddb7-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ddb7-120">-Name</span></span>
<span data-ttu-id="4ddb7-121">Especifica o nome da tabela a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddb7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ddb7-122">-PassThru</span></span>
<span data-ttu-id="4ddb7-123">Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4ddb7-124">Por padrão, esse cmdlet não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4ddb7-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ddb7-125">-Confirm</span></span>
<span data-ttu-id="4ddb7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ddb7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ddb7-127">-WhatIf</span></span>
<span data-ttu-id="4ddb7-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ddb7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ddb7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddb7-130">CommonParameters</span></span>
<span data-ttu-id="4ddb7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ddb7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddb7-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddb7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddb7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ddb7-133">INPUTS</span></span>

### <span data-ttu-id="4ddb7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4ddb7-134">System.String</span></span>

### <span data-ttu-id="4ddb7-135">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ddb7-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ddb7-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ddb7-136">OUTPUTS</span></span>

### <span data-ttu-id="4ddb7-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ddb7-137">System.Boolean</span></span>

## <span data-ttu-id="4ddb7-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ddb7-138">NOTES</span></span>

## <span data-ttu-id="4ddb7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ddb7-139">RELATED LINKS</span></span>

[<span data-ttu-id="4ddb7-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="4ddb7-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
