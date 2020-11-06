---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 7df59f75200bbc0d52c595c263228d7bf9801486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596809"
---
# <span data-ttu-id="bf373-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="bf373-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="bf373-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf373-102">SYNOPSIS</span></span>
<span data-ttu-id="bf373-103">Restaurar um arquivo ou uma pasta excluída no Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="bf373-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="bf373-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf373-104">SYNTAX</span></span>

### <span data-ttu-id="bf373-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf373-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf373-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="bf373-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf373-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf373-107">DESCRIPTION</span></span>
<span data-ttu-id="bf373-108">O cmdlet **Restore-AzDataLakeStoreDeletedItem** restaura um arquivo ou uma pasta excluída no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="bf373-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="bf373-109">Requer o caminho do item excluído no lixo retornado por Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="bf373-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="bf373-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf373-110">EXAMPLES</span></span>

### <span data-ttu-id="bf373-111">Exemplo 1: restaurar um arquivo do data Lake Store usando a opção-Force</span><span class="sxs-lookup"><span data-stu-id="bf373-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="bf373-112">OS</span><span class="sxs-lookup"><span data-stu-id="bf373-112">PARAMETERS</span></span>

### <span data-ttu-id="bf373-113">-Conta</span><span class="sxs-lookup"><span data-stu-id="bf373-113">-Account</span></span>
<span data-ttu-id="bf373-114">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bf373-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="bf373-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf373-115">-DefaultProfile</span></span>
<span data-ttu-id="bf373-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf373-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf373-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="bf373-117">-DeletedItem</span></span>
<span data-ttu-id="bf373-118">O objeto de item excluído.</span><span class="sxs-lookup"><span data-stu-id="bf373-118">The deleted item object.</span></span>

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

### <span data-ttu-id="bf373-119">-Destino</span><span class="sxs-lookup"><span data-stu-id="bf373-119">-Destination</span></span>
<span data-ttu-id="bf373-120">O caminho de destino para o qual o arquivo ou a pasta excluída deve ser restaurado.</span><span class="sxs-lookup"><span data-stu-id="bf373-120">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="bf373-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf373-121">-Force</span></span>
<span data-ttu-id="bf373-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bf373-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf373-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf373-123">-PassThru</span></span>
<span data-ttu-id="bf373-124">Retorna booliano true no sucesso.</span><span class="sxs-lookup"><span data-stu-id="bf373-124">Return boolean true on success.</span></span>

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

### <span data-ttu-id="bf373-125">-Caminho</span><span class="sxs-lookup"><span data-stu-id="bf373-125">-Path</span></span>
<span data-ttu-id="bf373-126">O caminho do arquivo ou da pasta excluída no lixo.</span><span class="sxs-lookup"><span data-stu-id="bf373-126">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="bf373-127">-Restoreaction</span><span class="sxs-lookup"><span data-stu-id="bf373-127">-RestoreAction</span></span>
<span data-ttu-id="bf373-128">Ação a ser tomada em conflito com o nome do destino-"cópia" ou "substituir"</span><span class="sxs-lookup"><span data-stu-id="bf373-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="bf373-129">-Digite</span><span class="sxs-lookup"><span data-stu-id="bf373-129">-Type</span></span>
<span data-ttu-id="bf373-130">O tipo de entrada sendo restaurado-"arquivo" ou "pasta"</span><span class="sxs-lookup"><span data-stu-id="bf373-130">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="bf373-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf373-131">CommonParameters</span></span>
<span data-ttu-id="bf373-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf373-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf373-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf373-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf373-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf373-134">INPUTS</span></span>

### <span data-ttu-id="bf373-135">System. String</span><span class="sxs-lookup"><span data-stu-id="bf373-135">System.String</span></span>

## <span data-ttu-id="bf373-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf373-136">OUTPUTS</span></span>

### <span data-ttu-id="bf373-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bf373-137">None</span></span>

## <span data-ttu-id="bf373-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf373-138">NOTES</span></span>

## <span data-ttu-id="bf373-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf373-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf373-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="bf373-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)