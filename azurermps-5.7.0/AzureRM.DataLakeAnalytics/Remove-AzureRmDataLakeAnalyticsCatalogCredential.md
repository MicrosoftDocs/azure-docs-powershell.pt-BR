---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C6BB6E4D-6009-4796-866B-17115FDFA06D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: af6acce52ee41297e650abb76188324ecf313679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428947"
---
# <span data-ttu-id="7a409-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="7a409-101">Remove-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="7a409-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7a409-102">SYNOPSIS</span></span>
<span data-ttu-id="7a409-103">Exclui uma credencial do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a409-103">Deletes an Azure Data Lake Analytics credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a409-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a409-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String> [-Name] <String>
 [[-Password] <PSCredential>] [-Recurse] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a409-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7a409-105">DESCRIPTION</span></span>
<span data-ttu-id="7a409-106">O cmdlet Remove-AzureRmDataLakeAnalyticsCatalogCredential exclui uma credencial do catálogo do Azure data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a409-106">The Remove-AzureRmDataLakeAnalyticsCatalogCredential cmdlet deletes an Azure Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="7a409-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a409-107">EXAMPLES</span></span>

### <span data-ttu-id="7a409-108">Exemplo 1: remover uma credencial</span><span class="sxs-lookup"><span data-stu-id="7a409-108">Example 1: Remove a credential</span></span>
```
PS C:\> Remove-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdla" `
                      -DatabaseName "DatabaseName" `
                      -Name "CredName"
```

<span data-ttu-id="7a409-109">Este comando Remove a credencial de catálogo do data Lake Analytics especificada.</span><span class="sxs-lookup"><span data-stu-id="7a409-109">This command removes the specified Data Lake Analytics catalog credential.</span></span>

## <span data-ttu-id="7a409-110">OS</span><span class="sxs-lookup"><span data-stu-id="7a409-110">PARAMETERS</span></span>

### <span data-ttu-id="7a409-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="7a409-111">-Account</span></span>
<span data-ttu-id="7a409-112">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7a409-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a409-113">-DatabaseName</span></span>
<span data-ttu-id="7a409-114">Especifica o nome do banco de dados que contém a credencial.</span><span class="sxs-lookup"><span data-stu-id="7a409-114">Specifies the name of the database that holds the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a409-115">-DefaultProfile</span></span>
<span data-ttu-id="7a409-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7a409-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7a409-117">-Force</span></span>
<span data-ttu-id="7a409-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7a409-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7a409-119">-Name</span></span>
<span data-ttu-id="7a409-120">Especifica o nome da credencial.</span><span class="sxs-lookup"><span data-stu-id="7a409-120">Specifies the name of the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a409-121">-PassThru</span></span>
<span data-ttu-id="7a409-122">Indica que esse cmdlet não aguarda a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="7a409-122">Indicates that this cmdlet does not wait for the operation to complete.</span></span>
<span data-ttu-id="7a409-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7a409-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7a409-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7a409-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="7a409-125">-Password</span></span>
<span data-ttu-id="7a409-126">A senha da credencial.</span><span class="sxs-lookup"><span data-stu-id="7a409-126">The password for the credential.</span></span>
<span data-ttu-id="7a409-127">Isso é necessário se o chamador não for o proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="7a409-127">This is required if the caller is not the owner of the account.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="7a409-128">-Recurse</span></span>
<span data-ttu-id="7a409-129">Indica que essa operação de exclusão deve passar e também excluir e cancelar todos os recursos dependentes dessa credencial.</span><span class="sxs-lookup"><span data-stu-id="7a409-129">Indicates that this delete operation should go through and also delete and drop all resources dependent on this credential.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7a409-130">-Confirm</span></span>
<span data-ttu-id="7a409-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a409-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a409-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a409-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a409-133">CommonParameters</span></span>
<span data-ttu-id="7a409-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a409-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a409-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a409-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a409-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7a409-136">INPUTS</span></span>

### <span data-ttu-id="7a409-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7a409-137">None</span></span>
<span data-ttu-id="7a409-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="7a409-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a409-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7a409-139">OUTPUTS</span></span>

### <span data-ttu-id="7a409-140">bool</span><span class="sxs-lookup"><span data-stu-id="7a409-140">bool</span></span>
<span data-ttu-id="7a409-141">Se PassThru for especificado, retornará true após a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="7a409-141">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="7a409-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7a409-142">NOTES</span></span>

## <span data-ttu-id="7a409-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a409-143">RELATED LINKS</span></span>

