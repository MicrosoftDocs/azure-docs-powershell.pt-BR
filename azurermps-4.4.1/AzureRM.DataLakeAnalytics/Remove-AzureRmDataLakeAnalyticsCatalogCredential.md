---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: fc25b0a6605632da44d2b198c4bb30c515b2e456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427955"
---
# <span data-ttu-id="8f974-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="8f974-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="8f974-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f974-102">SYNOPSIS</span></span>
<span data-ttu-id="8f974-103">Exclui uma credencial do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8f974-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f974-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f974-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f974-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8f974-105">DESCRIPTION</span></span>
<span data-ttu-id="8f974-106">O cmdlet Remove-AzureRmDataLakeAnalyticsCatalogCredential exclui uma credencial do catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8f974-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8f974-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8f974-107">EXAMPLES</span></span>

### <span data-ttu-id="8f974-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="8f974-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="8f974-109">Este comando Remove a credencial de catálogo do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="8f974-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="8f974-110">OS</span><span class="sxs-lookup"><span data-stu-id="8f974-110">PARAMETERS</span></span>

### <span data-ttu-id="8f974-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="8f974-111">-Account</span></span>
<span data-ttu-id="8f974-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8f974-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="8f974-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f974-113">-DatabaseName</span></span>
<span data-ttu-id="8f974-114">Especifica o nome do banco de dados que contém a credencial.</span><span class="sxs-lookup"><span data-stu-id="8f974-114">Specifies the name of the database that holds the credential.</span></span>

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

### <span data-ttu-id="8f974-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f974-115">-Force</span></span>
<span data-ttu-id="8f974-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8f974-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8f974-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f974-117">-Name</span></span>
<span data-ttu-id="8f974-118">Especifica o nome da credencial.</span><span class="sxs-lookup"><span data-stu-id="8f974-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="8f974-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f974-119">-PassThru</span></span>
<span data-ttu-id="8f974-120">Indica que esse cmdlet não aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="8f974-120">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="8f974-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8f974-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f974-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8f974-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f974-123">-Senha</span><span class="sxs-lookup"><span data-stu-id="8f974-123">-Password</span></span>
<span data-ttu-id="8f974-124">A senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="8f974-124">The password for the credential.</span></span>
<span data-ttu-id="8f974-125">Isso é necessário se o chamador não for o proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="8f974-125">This is required if the caller is not the owner of the account.</span></span>

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

### <span data-ttu-id="8f974-126">-Recurse</span><span class="sxs-lookup"><span data-stu-id="8f974-126">-Recurse</span></span>
<span data-ttu-id="8f974-127">Indica que essa operação de exclusão deve passar e também excluir e cancelar todos os recursos dependentes dessa credencial.</span><span class="sxs-lookup"><span data-stu-id="8f974-127">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

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

### <span data-ttu-id="8f974-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8f974-128">-Confirm</span></span>
<span data-ttu-id="8f974-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f974-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f974-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f974-130">-WhatIf</span></span>
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

### <span data-ttu-id="8f974-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f974-131">-DefaultProfile</span></span>
<span data-ttu-id="8f974-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f974-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f974-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f974-133">CommonParameters</span></span>
<span data-ttu-id="8f974-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f974-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f974-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f974-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f974-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8f974-136">INPUTS</span></span>

## <span data-ttu-id="8f974-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8f974-137">OUTPUTS</span></span>

### <span data-ttu-id="8f974-138">bool</span><span class="sxs-lookup"><span data-stu-id="8f974-138">bool</span></span>
<span data-ttu-id="8f974-139">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="8f974-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8f974-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8f974-140">NOTES</span></span>

## <span data-ttu-id="8f974-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f974-141">RELATED LINKS</span></span>

