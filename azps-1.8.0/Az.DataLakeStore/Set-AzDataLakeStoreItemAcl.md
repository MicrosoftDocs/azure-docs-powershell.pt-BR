---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770912"
---
# <span data-ttu-id="1b82f-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="1b82f-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="1b82f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1b82f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b82f-103">Modifica a ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b82f-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1b82f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b82f-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b82f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1b82f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b82f-106">O cmdlet **set-AzDataLakeStoreItemAcl** modifica a ACL (lista de controle de acesso) de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="1b82f-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1b82f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b82f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b82f-108">Exemplo 1: definir a ACL para um arquivo e uma pasta</span><span class="sxs-lookup"><span data-stu-id="1b82f-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="1b82f-109">O primeiro comando obtém a ACL para o diretório raiz da conta do ContosoADL e, em seguida, armazena-o na variável $ACL.</span><span class="sxs-lookup"><span data-stu-id="1b82f-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="1b82f-110">O segundo comando define a ACL do arquivo Test.txt como a do $ACL.</span><span class="sxs-lookup"><span data-stu-id="1b82f-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="1b82f-111">Exemplo 2: definir a ACL para a pasta recursivamente</span><span class="sxs-lookup"><span data-stu-id="1b82f-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="1b82f-112">O primeiro comando obtém a ACL para o diretório Pasta1 da conta ContosoADL e, em seguida, armazena-o na variável $ACL.</span><span class="sxs-lookup"><span data-stu-id="1b82f-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="1b82f-113">O segundo comando define a ACL recursivamente para Pasta2 e seus subdiretórios e arquivos para o mesmo em $ACL.</span><span class="sxs-lookup"><span data-stu-id="1b82f-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="1b82f-114">OS</span><span class="sxs-lookup"><span data-stu-id="1b82f-114">PARAMETERS</span></span>

### <span data-ttu-id="1b82f-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="1b82f-115">-Account</span></span>
<span data-ttu-id="1b82f-116">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1b82f-116">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="1b82f-117">-Acl</span></span>
<span data-ttu-id="1b82f-118">Especifica uma ACL para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1b82f-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-119">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="1b82f-119">-Concurrency</span></span>
<span data-ttu-id="1b82f-120">Número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="1b82f-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="1b82f-121">Opcional: um padrão razoável será selecionado.</span><span class="sxs-lookup"><span data-stu-id="1b82f-121">Optional: a reasonable default will be selected.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b82f-122">-DefaultProfile</span></span>
<span data-ttu-id="1b82f-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1b82f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b82f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b82f-124">-PassThru</span></span>
<span data-ttu-id="1b82f-125">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="1b82f-125">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-126">-Caminho</span><span class="sxs-lookup"><span data-stu-id="1b82f-126">-Path</span></span>
<span data-ttu-id="1b82f-127">Especifica o caminho do repositório data Lake do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="1b82f-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="1b82f-128">-Recurse</span></span>
<span data-ttu-id="1b82f-129">Indica a ACL a ser definida recursivamente para as subpastas e arquivos filho</span><span class="sxs-lookup"><span data-stu-id="1b82f-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b82f-130">-Progresso</span><span class="sxs-lookup"><span data-stu-id="1b82f-130">-ShowProgress</span></span>
<span data-ttu-id="1b82f-131">Se for passado, o status do progresso será mostrado.</span><span class="sxs-lookup"><span data-stu-id="1b82f-131">If passed then progress status is showed.</span></span> <span data-ttu-id="1b82f-132">Aplicável somente quando o conjunto de ACLs recursivas está concluído.</span><span class="sxs-lookup"><span data-stu-id="1b82f-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="1b82f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1b82f-133">-Confirm</span></span>
<span data-ttu-id="1b82f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b82f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b82f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b82f-135">-WhatIf</span></span>
<span data-ttu-id="1b82f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1b82f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b82f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1b82f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b82f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b82f-138">CommonParameters</span></span>
<span data-ttu-id="1b82f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b82f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b82f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b82f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b82f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1b82f-141">INPUTS</span></span>

### <span data-ttu-id="1b82f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1b82f-142">System.String</span></span>

### <span data-ttu-id="1b82f-143">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1b82f-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1b82f-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="1b82f-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="1b82f-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1b82f-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1b82f-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1b82f-146">System.Int32</span></span>

## <span data-ttu-id="1b82f-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1b82f-147">OUTPUTS</span></span>

### <span data-ttu-id="1b82f-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="1b82f-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="1b82f-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1b82f-149">NOTES</span></span>

## <span data-ttu-id="1b82f-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b82f-150">RELATED LINKS</span></span>
