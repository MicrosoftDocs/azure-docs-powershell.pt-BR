---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955634"
---
# <span data-ttu-id="2c43b-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2c43b-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="2c43b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c43b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c43b-103">Restaurar um arquivo ou uma pasta excluída no Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="2c43b-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="2c43b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c43b-104">SYNTAX</span></span>

### <span data-ttu-id="2c43b-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c43b-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c43b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2c43b-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c43b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c43b-107">DESCRIPTION</span></span>
<span data-ttu-id="2c43b-108">O cmdlet **Restore-AzDataLakeStoreDeletedItem** restaura um arquivo ou uma pasta excluída no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="2c43b-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="2c43b-109">Requer o caminho do item excluído no lixo retornado por Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="2c43b-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="2c43b-110">Cuidado: não excluir arquivos é uma melhor operação de esforço.</span><span class="sxs-lookup"><span data-stu-id="2c43b-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="2c43b-111">Não há garantias de que um arquivo possa ser restaurado depois que ele é excluído.</span><span class="sxs-lookup"><span data-stu-id="2c43b-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="2c43b-112">O uso dessa API é habilitado por meio da lista branca.</span><span class="sxs-lookup"><span data-stu-id="2c43b-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="2c43b-113">Se a sua conta do ADL não for listada, o uso dessa API irá gerar uma exceção não implementada.</span><span class="sxs-lookup"><span data-stu-id="2c43b-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="2c43b-114">Para obter mais informações e assistência, entre em contato com o suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c43b-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="2c43b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c43b-115">EXAMPLES</span></span>

### <span data-ttu-id="2c43b-116">Exemplo 1: restaurar um arquivo do data Lake Store usando a opção-Force</span><span class="sxs-lookup"><span data-stu-id="2c43b-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="2c43b-117">OS</span><span class="sxs-lookup"><span data-stu-id="2c43b-117">PARAMETERS</span></span>

### <span data-ttu-id="2c43b-118">-Conta</span><span class="sxs-lookup"><span data-stu-id="2c43b-118">-Account</span></span>
<span data-ttu-id="2c43b-119">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c43b-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2c43b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c43b-120">-DefaultProfile</span></span>
<span data-ttu-id="2c43b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c43b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c43b-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="2c43b-122">-DeletedItem</span></span>
<span data-ttu-id="2c43b-123">O objeto de item excluído.</span><span class="sxs-lookup"><span data-stu-id="2c43b-123">The deleted item object.</span></span>

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

### <span data-ttu-id="2c43b-124">-Destino</span><span class="sxs-lookup"><span data-stu-id="2c43b-124">-Destination</span></span>
<span data-ttu-id="2c43b-125">O caminho de destino para o qual o arquivo ou a pasta excluída deve ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="2c43b-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="2c43b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2c43b-126">-Force</span></span>
<span data-ttu-id="2c43b-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="2c43b-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c43b-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c43b-128">-PassThru</span></span>
<span data-ttu-id="2c43b-129">Retorna booliano true no sucesso.</span><span class="sxs-lookup"><span data-stu-id="2c43b-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="2c43b-130">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2c43b-130">-Path</span></span>
<span data-ttu-id="2c43b-131">O caminho do arquivo ou da pasta excluída no lixo.</span><span class="sxs-lookup"><span data-stu-id="2c43b-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="2c43b-132">-Restoreaction</span><span class="sxs-lookup"><span data-stu-id="2c43b-132">-RestoreAction</span></span>
<span data-ttu-id="2c43b-133">Ação a ser tomada em conflito com o nome do destino-"cópia" ou "substituir"</span><span class="sxs-lookup"><span data-stu-id="2c43b-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="2c43b-134">-Digite</span><span class="sxs-lookup"><span data-stu-id="2c43b-134">-Type</span></span>
<span data-ttu-id="2c43b-135">O tipo de entrada sendo restaurado-"arquivo" ou "pasta"</span><span class="sxs-lookup"><span data-stu-id="2c43b-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="2c43b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c43b-136">CommonParameters</span></span>
<span data-ttu-id="2c43b-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c43b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c43b-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c43b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c43b-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c43b-139">INPUTS</span></span>

### <span data-ttu-id="2c43b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c43b-140">System.String</span></span>

## <span data-ttu-id="2c43b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c43b-141">OUTPUTS</span></span>

### <span data-ttu-id="2c43b-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2c43b-142">None</span></span>

## <span data-ttu-id="2c43b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c43b-143">NOTES</span></span>

## <span data-ttu-id="2c43b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c43b-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c43b-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2c43b-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)