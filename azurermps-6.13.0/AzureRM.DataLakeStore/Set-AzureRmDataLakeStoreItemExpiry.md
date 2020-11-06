---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 4aff82a2621a462f0af14fe2dce620f297011874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429578"
---
# <span data-ttu-id="5dbe3-101">Set-AzureRmDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="5dbe3-101">Set-AzureRmDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="5dbe3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5dbe3-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbe3-103">Define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dbe3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5dbe3-104">SYNTAX</span></span>

### <span data-ttu-id="5dbe3-105">SetAbsoluteNeverExpireExpiry (padrão)</span><span class="sxs-lookup"><span data-stu-id="5dbe3-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dbe3-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="5dbe3-106">SetRelativeExpiry</span></span>
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dbe3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5dbe3-107">DESCRIPTION</span></span>
<span data-ttu-id="5dbe3-108">O cmdlet **set-AzureRmDataLakeStoreItemExpiry** define ou remove o tempo de expiração de um arquivo em uma conta do Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-108">The **Set-AzureRmDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="5dbe3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5dbe3-109">EXAMPLES</span></span>

### <span data-ttu-id="5dbe3-110">Exemplo 1: definir o tempo de expiração de um arquivo</span><span class="sxs-lookup"><span data-stu-id="5dbe3-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="5dbe3-111">Define a expiração no arquivo myfile.txt na conta ContosoADL para ser de duas horas a partir de agora.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="5dbe3-112">Isso fará com que o arquivo expire (ser marcado para exclusão) em duas horas.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="5dbe3-113">Exemplo 2: remover a expiração em um arquivo</span><span class="sxs-lookup"><span data-stu-id="5dbe3-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="5dbe3-114">Remove qualquer expiração definida anteriormente no arquivo ' myfile.txt ' na conta ' ContosoADL '.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="5dbe3-115">Isso significa que o arquivo não expirará automaticamente (será marcado para exclusão) e precisará ser excluído manualmente ou definido para expirar novamente.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="5dbe3-116">Exemplo 3: definir a hora de expiração para um arquivo relativo a agora</span><span class="sxs-lookup"><span data-stu-id="5dbe3-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="5dbe3-117">O primeiro comando define o tempo de expiração do arquivo/myfile.txt 240 segundos relativo à hora atual no servidor.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="5dbe3-118">O segundo comando define o tempo de expiração do arquivo/myfile.txt 240 segundos relativo à hora da criação no servidor.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="5dbe3-119">OS</span><span class="sxs-lookup"><span data-stu-id="5dbe3-119">PARAMETERS</span></span>

### <span data-ttu-id="5dbe3-120">-Conta</span><span class="sxs-lookup"><span data-stu-id="5dbe3-120">-Account</span></span>
<span data-ttu-id="5dbe3-121">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="5dbe3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbe3-122">-DefaultProfile</span></span>
<span data-ttu-id="5dbe3-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dbe3-124">-Expiração</span><span class="sxs-lookup"><span data-stu-id="5dbe3-124">-Expiration</span></span>
<span data-ttu-id="5dbe3-125">O tempo de expiração absoluto do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="5dbe3-126">Se nenhum valor ou for definido como MaxValue, o arquivo nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-126">If no value or set to MaxValue, the file will never expire.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbe3-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="5dbe3-127">-Path</span></span>
<span data-ttu-id="5dbe3-128">Especifica o caminho do repositório data Lake do item de arquivo para o qual definir ou remover a expiração.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="5dbe3-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="5dbe3-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="5dbe3-130">Opções de expiração relativas.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-130">Relative expiry options.</span></span> <span data-ttu-id="5dbe3-131">RelativeToNow ou RelativeToCreationDate são opções atuais</span><span class="sxs-lookup"><span data-stu-id="5dbe3-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbe3-132">-Relativetime</span><span class="sxs-lookup"><span data-stu-id="5dbe3-132">-RelativeTime</span></span>
<span data-ttu-id="5dbe3-133">O tempo relativo em milissegundos em relação ao momento ou à hora da criação</span><span class="sxs-lookup"><span data-stu-id="5dbe3-133">The relative time in milliseconds with respect to now or creation time</span></span>

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbe3-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5dbe3-134">-Confirm</span></span>
<span data-ttu-id="5dbe3-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dbe3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dbe3-136">-WhatIf</span></span>
<span data-ttu-id="5dbe3-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dbe3-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dbe3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbe3-139">CommonParameters</span></span>
<span data-ttu-id="5dbe3-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbe3-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dbe3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbe3-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5dbe3-142">INPUTS</span></span>

### <span data-ttu-id="5dbe3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5dbe3-143">System.String</span></span>

### <span data-ttu-id="5dbe3-144">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="5dbe3-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="5dbe3-145">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5dbe3-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="5dbe3-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="5dbe3-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="5dbe3-147">System. Int64</span><span class="sxs-lookup"><span data-stu-id="5dbe3-147">System.Int64</span></span>

## <span data-ttu-id="5dbe3-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5dbe3-148">OUTPUTS</span></span>

### <span data-ttu-id="5dbe3-149">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dbe3-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="5dbe3-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5dbe3-150">NOTES</span></span>
<span data-ttu-id="5dbe3-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="5dbe3-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="5dbe3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5dbe3-152">RELATED LINKS</span></span>

[<span data-ttu-id="5dbe3-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dbe3-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)
