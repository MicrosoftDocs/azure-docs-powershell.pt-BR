---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 9b762a2fe0f12483fd664b8862e483b1b948bc75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887777"
---
# <span data-ttu-id="771db-101">Remove-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="771db-101">Remove-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="771db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="771db-102">SYNOPSIS</span></span>
<span data-ttu-id="771db-103">Limpa a ACL de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="771db-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="771db-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="771db-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="771db-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="771db-105">DESCRIPTION</span></span>
<span data-ttu-id="771db-106">O cmdlet **Remove-AzDataLakeStoreItemAcl** limpa a lista de controles de acesso (ACL) de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="771db-106">The **Remove-AzDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="771db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="771db-107">EXAMPLES</span></span>

### <span data-ttu-id="771db-108">Exemplo 1: Remover a ACL de uma pasta</span><span class="sxs-lookup"><span data-stu-id="771db-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="771db-109">Este comando remove a ACL do diretório raiz da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="771db-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="771db-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="771db-110">PARAMETERS</span></span>

### <span data-ttu-id="771db-111">-Account</span><span class="sxs-lookup"><span data-stu-id="771db-111">-Account</span></span>
<span data-ttu-id="771db-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="771db-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="771db-113">-Default</span><span class="sxs-lookup"><span data-stu-id="771db-113">-Default</span></span>
<span data-ttu-id="771db-114">Indica que o cmdlet remove a ACL padrão para um arquivo ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="771db-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771db-115">-DefaultProfile</span></span>
<span data-ttu-id="771db-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="771db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="771db-117">-Force</span><span class="sxs-lookup"><span data-stu-id="771db-117">-Force</span></span>
<span data-ttu-id="771db-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="771db-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="771db-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="771db-119">-PassThru</span></span>
<span data-ttu-id="771db-120">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="771db-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="771db-121">-Path</span><span class="sxs-lookup"><span data-stu-id="771db-121">-Path</span></span>
<span data-ttu-id="771db-122">Especifica o caminho do Data Lake Store do item, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="771db-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="771db-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="771db-123">-Confirm</span></span>
<span data-ttu-id="771db-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="771db-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="771db-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="771db-125">-WhatIf</span></span>
<span data-ttu-id="771db-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="771db-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="771db-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="771db-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="771db-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771db-128">CommonParameters</span></span>
<span data-ttu-id="771db-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="771db-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771db-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="771db-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771db-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="771db-131">INPUTS</span></span>

### <span data-ttu-id="771db-132">System.String</span><span class="sxs-lookup"><span data-stu-id="771db-132">System.String</span></span>

### <span data-ttu-id="771db-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="771db-133">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="771db-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="771db-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="771db-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="771db-135">OUTPUTS</span></span>

### <span data-ttu-id="771db-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="771db-136">System.Boolean</span></span>

## <span data-ttu-id="771db-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="771db-137">NOTES</span></span>
* <span data-ttu-id="771db-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="771db-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="771db-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="771db-139">RELATED LINKS</span></span>

[<span data-ttu-id="771db-140">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="771db-140">Get-AzDataLakeStoreItemAclEntry</span></span>](./Get-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="771db-141">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="771db-141">Set-AzDataLakeStoreItemAcl</span></span>](./Set-AzDataLakeStoreItemAcl.md)

[<span data-ttu-id="771db-142">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="771db-142">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


