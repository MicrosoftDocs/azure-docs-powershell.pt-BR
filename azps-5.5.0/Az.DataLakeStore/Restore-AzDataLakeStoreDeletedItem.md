---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115376"
---
# <span data-ttu-id="f0196-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f0196-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="f0196-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0196-102">SYNOPSIS</span></span>
<span data-ttu-id="f0196-103">Restaure um arquivo ou pasta excluído no Lago de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0196-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="f0196-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0196-104">SYNTAX</span></span>

### <span data-ttu-id="f0196-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f0196-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0196-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="f0196-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0196-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0196-107">DESCRIPTION</span></span>
<span data-ttu-id="f0196-108">O cmdlet **Restore-AzDataLakeStoreDeletedItem** restaura um arquivo ou pasta excluído no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f0196-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="f0196-109">Requer o caminho do item excluído na lixeira retornado pela Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="f0196-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="f0196-110">Cuidado: a reseleção de arquivos é uma operação de melhor esforço.</span><span class="sxs-lookup"><span data-stu-id="f0196-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="f0196-111">Não há garantias de que um arquivo possa ser restaurado depois de excluído.</span><span class="sxs-lookup"><span data-stu-id="f0196-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="f0196-112">O uso dessa API está habilitado por meio da lista de contatos.</span><span class="sxs-lookup"><span data-stu-id="f0196-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="f0196-113">Se sua conta do ADL não estiver listada em branco, o uso dessa api lançará exceção não implementada.</span><span class="sxs-lookup"><span data-stu-id="f0196-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="f0196-114">Para obter mais informações e assistência, entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f0196-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="f0196-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f0196-115">EXAMPLES</span></span>

### <span data-ttu-id="f0196-116">Exemplo 1: Restaurar um arquivo do Data Lake Store usando a opção -force</span><span class="sxs-lookup"><span data-stu-id="f0196-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="f0196-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0196-117">PARAMETERS</span></span>

### <span data-ttu-id="f0196-118">-Conta</span><span class="sxs-lookup"><span data-stu-id="f0196-118">-Account</span></span>
<span data-ttu-id="f0196-119">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f0196-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f0196-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0196-120">-DefaultProfile</span></span>
<span data-ttu-id="f0196-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f0196-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0196-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="f0196-122">-DeletedItem</span></span>
<span data-ttu-id="f0196-123">O objeto de item excluído.</span><span class="sxs-lookup"><span data-stu-id="f0196-123">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0196-124">-Destino</span><span class="sxs-lookup"><span data-stu-id="f0196-124">-Destination</span></span>
<span data-ttu-id="f0196-125">O caminho de destino para onde o arquivo ou pasta excluído deve ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="f0196-125">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0196-126">-Forçar</span><span class="sxs-lookup"><span data-stu-id="f0196-126">-Force</span></span>
<span data-ttu-id="f0196-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0196-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0196-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0196-128">-PassThru</span></span>
<span data-ttu-id="f0196-129">Retorne booliana verdadeiro sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="f0196-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="f0196-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="f0196-130">-Path</span></span>
<span data-ttu-id="f0196-131">O caminho do arquivo ou pasta excluído na lixeira.</span><span class="sxs-lookup"><span data-stu-id="f0196-131">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0196-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="f0196-132">-RestoreAction</span></span>
<span data-ttu-id="f0196-133">Ação a ser tomada sobre conflitos de nome de destino - "copiar" ou "substituir"</span><span class="sxs-lookup"><span data-stu-id="f0196-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0196-134">-Tipo</span><span class="sxs-lookup"><span data-stu-id="f0196-134">-Type</span></span>
<span data-ttu-id="f0196-135">O tipo de entrada que está sendo restaurado - "arquivo" ou "pasta"</span><span class="sxs-lookup"><span data-stu-id="f0196-135">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0196-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0196-136">CommonParameters</span></span>
<span data-ttu-id="f0196-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0196-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0196-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0196-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0196-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="f0196-139">INPUTS</span></span>

### <span data-ttu-id="f0196-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f0196-140">System.String</span></span>

## <span data-ttu-id="f0196-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="f0196-141">OUTPUTS</span></span>

### <span data-ttu-id="f0196-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0196-142">None</span></span>

## <span data-ttu-id="f0196-143">Notas</span><span class="sxs-lookup"><span data-stu-id="f0196-143">NOTES</span></span>

## <span data-ttu-id="f0196-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0196-144">RELATED LINKS</span></span>

[<span data-ttu-id="f0196-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="f0196-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)