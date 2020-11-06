---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441560"
---
# <span data-ttu-id="3f23e-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="3f23e-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="3f23e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f23e-102">SYNOPSIS</span></span>
<span data-ttu-id="3f23e-103">Define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f23e-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f23e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f23e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f23e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f23e-105">DESCRIPTION</span></span>
<span data-ttu-id="3f23e-106">O cmdlet **set-AzureRmDataLakeStoreItemExpiry** define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f23e-106">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="3f23e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f23e-107">EXAMPLES</span></span>

### <span data-ttu-id="3f23e-108">Exemplo 1: definir o tempo de expiração de um arquivo</span><span class="sxs-lookup"><span data-stu-id="3f23e-108">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="3f23e-109">Define a expiração no arquivo myfile.txt na conta ContosoADL para ser de duas horas a partir de agora.</span><span class="sxs-lookup"><span data-stu-id="3f23e-109">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="3f23e-110">Isso fará com que o arquivo expire (ser marcado para exclusão) em duas horas.</span><span class="sxs-lookup"><span data-stu-id="3f23e-110">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="3f23e-111">Exemplo 2: remover a expiração em um arquivo</span><span class="sxs-lookup"><span data-stu-id="3f23e-111">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="3f23e-112">Remove qualquer expiração definida anteriormente no arquivo ' myfile.txt ' na conta ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="3f23e-112">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="3f23e-113">Isso significa que o arquivo não expirará automaticamente (será marcado para exclusão) e precisará ser excluído manualmente ou definido para expirar novamente.</span><span class="sxs-lookup"><span data-stu-id="3f23e-113">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

## <span data-ttu-id="3f23e-114">OS</span><span class="sxs-lookup"><span data-stu-id="3f23e-114">PARAMETERS</span></span>

### <span data-ttu-id="3f23e-115">-Conta</span><span class="sxs-lookup"><span data-stu-id="3f23e-115">-Account</span></span>
<span data-ttu-id="3f23e-116">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f23e-116">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="3f23e-117">-Expiração</span><span class="sxs-lookup"><span data-stu-id="3f23e-117">-Expiration</span></span>
<span data-ttu-id="3f23e-118">O tempo de expiração absoluto do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3f23e-118">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="3f23e-119">Se nenhum valor ou for definido como MaxValue, o arquivo nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="3f23e-119">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f23e-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3f23e-120">-Path</span></span>
<span data-ttu-id="3f23e-121">Especifica o caminho do repositório data Lake do item de arquivo para o qual definir ou remover a expiração.</span><span class="sxs-lookup"><span data-stu-id="3f23e-121">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="3f23e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f23e-122">-Confirm</span></span>
<span data-ttu-id="3f23e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f23e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f23e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f23e-124">-WhatIf</span></span>
<span data-ttu-id="3f23e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f23e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f23e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f23e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f23e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f23e-127">-DefaultProfile</span></span>
<span data-ttu-id="3f23e-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f23e-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f23e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f23e-129">CommonParameters</span></span>
<span data-ttu-id="3f23e-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f23e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f23e-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f23e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f23e-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f23e-132">INPUTS</span></span>

## <span data-ttu-id="3f23e-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f23e-133">OUTPUTS</span></span>

### <span data-ttu-id="3f23e-134">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3f23e-134">DataLakeStoreItem</span></span>
<span data-ttu-id="3f23e-135">O arquivo atualizado com um novo tempo de expiração.</span><span class="sxs-lookup"><span data-stu-id="3f23e-135">The updated file with a new expiration time.</span></span>

## <span data-ttu-id="3f23e-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f23e-136">NOTES</span></span>
<span data-ttu-id="3f23e-137">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="3f23e-137">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="3f23e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f23e-138">RELATED LINKS</span></span>

[<span data-ttu-id="3f23e-139">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3f23e-139">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

