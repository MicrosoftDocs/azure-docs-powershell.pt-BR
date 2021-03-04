---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 16663994a245a7429560ccf2ab855a84acc6ae57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885909"
---
# <span data-ttu-id="98e2a-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="98e2a-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="98e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="98e2a-103">Modifica a ACL de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="98e2a-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="98e2a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="98e2a-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e2a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="98e2a-105">DESCRIPTION</span></span>
<span data-ttu-id="98e2a-106">O cmdlet **Set-AzDataLakeStoreItemAcl** modifica a lista de controles de acesso (ACL) de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="98e2a-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="98e2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98e2a-107">EXAMPLES</span></span>

### <span data-ttu-id="98e2a-108">Exemplo 1: definir a ACL para um arquivo e uma pasta</span><span class="sxs-lookup"><span data-stu-id="98e2a-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="98e2a-109">O primeiro comando obtém o ACL para o diretório raiz da conta ContosoADL e o armazena na variável $ACL raiz.</span><span class="sxs-lookup"><span data-stu-id="98e2a-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="98e2a-110">O segundo comando define a ACL para o arquivo Test.txt como aquele em $ACL.</span><span class="sxs-lookup"><span data-stu-id="98e2a-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="98e2a-111">Exemplo 2: definir a ACL para pasta recursivamente</span><span class="sxs-lookup"><span data-stu-id="98e2a-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="98e2a-112">O primeiro comando obtém o ACL para o diretório Folder1 da conta ContosoADL e, em seguida, armazena-o na variável $ACL de diretório.</span><span class="sxs-lookup"><span data-stu-id="98e2a-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="98e2a-113">O segundo comando define a ACL recursivamente como Folder2 e seus sub-diretórios e arquivos como aquele em $ACL.</span><span class="sxs-lookup"><span data-stu-id="98e2a-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="98e2a-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="98e2a-114">PARAMETERS</span></span>

### <span data-ttu-id="98e2a-115">-Account</span><span class="sxs-lookup"><span data-stu-id="98e2a-115">-Account</span></span>
<span data-ttu-id="98e2a-116">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="98e2a-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="98e2a-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="98e2a-117">-Acl</span></span>
<span data-ttu-id="98e2a-118">Especifica um ACL para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="98e2a-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="98e2a-119">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="98e2a-119">-Concurrency</span></span>
<span data-ttu-id="98e2a-120">Número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="98e2a-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="98e2a-121">Opcional: um padrão razoável será selecionado.</span><span class="sxs-lookup"><span data-stu-id="98e2a-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="98e2a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e2a-122">-DefaultProfile</span></span>
<span data-ttu-id="98e2a-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="98e2a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98e2a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98e2a-124">-PassThru</span></span>
<span data-ttu-id="98e2a-125">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="98e2a-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="98e2a-126">-Path</span><span class="sxs-lookup"><span data-stu-id="98e2a-126">-Path</span></span>
<span data-ttu-id="98e2a-127">Especifica o caminho do Data Lake Store do arquivo ou pasta, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="98e2a-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="98e2a-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="98e2a-128">-Recurse</span></span>
<span data-ttu-id="98e2a-129">Indica a ACL a ser definida recursivamente para os subdiretivos filho e arquivos</span><span class="sxs-lookup"><span data-stu-id="98e2a-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="98e2a-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="98e2a-130">-ShowProgress</span></span>
<span data-ttu-id="98e2a-131">Se aprovado, o status de progresso será mostrado.</span><span class="sxs-lookup"><span data-stu-id="98e2a-131">If passed then progress status is showed.</span></span> <span data-ttu-id="98e2a-132">Aplicável somente quando o conjunto Acl recursivo é feito.</span><span class="sxs-lookup"><span data-stu-id="98e2a-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="98e2a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98e2a-133">-Confirm</span></span>
<span data-ttu-id="98e2a-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98e2a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e2a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e2a-135">-WhatIf</span></span>
<span data-ttu-id="98e2a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98e2a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e2a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98e2a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e2a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e2a-138">CommonParameters</span></span>
<span data-ttu-id="98e2a-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98e2a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e2a-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98e2a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e2a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98e2a-141">INPUTS</span></span>

### <span data-ttu-id="98e2a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="98e2a-142">System.String</span></span>

### <span data-ttu-id="98e2a-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="98e2a-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="98e2a-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="98e2a-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="98e2a-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98e2a-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="98e2a-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="98e2a-146">System.Int32</span></span>

## <span data-ttu-id="98e2a-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="98e2a-147">OUTPUTS</span></span>

### <span data-ttu-id="98e2a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="98e2a-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="98e2a-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="98e2a-149">NOTES</span></span>

## <span data-ttu-id="98e2a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98e2a-150">RELATED LINKS</span></span>
