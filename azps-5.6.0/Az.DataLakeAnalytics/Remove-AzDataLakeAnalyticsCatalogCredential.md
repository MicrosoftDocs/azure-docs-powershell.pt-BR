---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: f14448e7b7606f37f5ffdee8c944d48a557c1f0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891434"
---
# <span data-ttu-id="26e87-101">Remove-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="26e87-101">Remove-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="26e87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e87-102">SYNOPSIS</span></span>
<span data-ttu-id="26e87-103">Exclui uma credencial do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="26e87-103">Deletes an Azure Data Lake Analytics credential.</span></span>

## <span data-ttu-id="26e87-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26e87-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e87-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26e87-105">DESCRIPTION</span></span>
<span data-ttu-id="26e87-106">O Remove-AzDataLakeAnalyticsCatalogCredential cmdlet exclui uma credencial de catálogo do Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="26e87-106">The Remove-AzDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="26e87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26e87-107">EXAMPLES</span></span>

### <span data-ttu-id="26e87-108">Exemplo 1: Remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="26e87-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="26e87-109">Este comando remove a credencial de catálogo do Data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="26e87-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="26e87-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26e87-110">PARAMETERS</span></span>

### <span data-ttu-id="26e87-111">-Account</span><span class="sxs-lookup"><span data-stu-id="26e87-111">-Account</span></span>
<span data-ttu-id="26e87-112">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="26e87-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="26e87-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26e87-113">-DatabaseName</span></span>
<span data-ttu-id="26e87-114">Especifica o nome do banco de dados que contém a credencial.</span><span class="sxs-lookup"><span data-stu-id="26e87-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e87-115">-DefaultProfile</span></span>
<span data-ttu-id="26e87-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="26e87-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26e87-117">-Force</span><span class="sxs-lookup"><span data-stu-id="26e87-117">-Force</span></span>
<span data-ttu-id="26e87-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="26e87-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26e87-119">-Name</span><span class="sxs-lookup"><span data-stu-id="26e87-119">-Name</span></span>
<span data-ttu-id="26e87-120">Especifica o nome da credencial.</span><span class="sxs-lookup"><span data-stu-id="26e87-120">Specifies the name of the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e87-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26e87-121">-PassThru</span></span>
<span data-ttu-id="26e87-122">Indica que esse cmdlet não aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="26e87-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="26e87-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="26e87-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26e87-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="26e87-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26e87-125">-Password</span><span class="sxs-lookup"><span data-stu-id="26e87-125">-Password</span></span>
<span data-ttu-id="26e87-126">A senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="26e87-126">The password for the credential.</span></span>
<span data-ttu-id="26e87-127">Isso será necessário se o chamador não for o proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="26e87-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e87-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="26e87-128">-Recurse</span></span>
<span data-ttu-id="26e87-129">Indica que essa operação de exclusão deve passar e também excluir e soltar todos os recursos dependentes dessa credencial.</span><span class="sxs-lookup"><span data-stu-id="26e87-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="26e87-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26e87-130">-Confirm</span></span>
<span data-ttu-id="26e87-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e87-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e87-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e87-132">-WhatIf</span></span>
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

### <span data-ttu-id="26e87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e87-133">CommonParameters</span></span>
<span data-ttu-id="26e87-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e87-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e87-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e87-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26e87-136">INPUTS</span></span>

### <span data-ttu-id="26e87-137">System.String</span><span class="sxs-lookup"><span data-stu-id="26e87-137">System.String</span></span>

### <span data-ttu-id="26e87-138">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="26e87-138">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="26e87-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="26e87-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="26e87-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26e87-140">OUTPUTS</span></span>

### <span data-ttu-id="26e87-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26e87-141">System.Boolean</span></span>

## <span data-ttu-id="26e87-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="26e87-142">NOTES</span></span>

## <span data-ttu-id="26e87-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26e87-143">RELATED LINKS</span></span>
