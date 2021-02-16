---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemExpiry.md
ms.openlocfilehash: ff769801c7a3496ab094e5c9877e0b53fb64fbfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127028"
---
# <span data-ttu-id="d1b61-101">Set-AzDataLakeStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="d1b61-101">Set-AzDataLakeStoreItemExpiry</span></span>

## <span data-ttu-id="d1b61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1b61-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b61-103">Define ou remove o tempo de expiração de um arquivo em uma conta do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1b61-103">Sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="d1b61-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1b61-104">SYNTAX</span></span>

### <span data-ttu-id="d1b61-105">SetAbsoluteNeverExpireExpiry (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d1b61-105">SetAbsoluteNeverExpireExpiry (Default)</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1b61-106">SetRelativeExpiry</span><span class="sxs-lookup"><span data-stu-id="d1b61-106">SetRelativeExpiry</span></span>
```
Set-AzDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1b61-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1b61-107">DESCRIPTION</span></span>
<span data-ttu-id="d1b61-108">O cmdlet **Set-AzDataLakeStoreItemExpiry** define ou remove o tempo de expiração de um arquivo em uma conta do Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1b61-108">The **Set-AzDataLakeStoreItemExpiry** cmdlet sets or removes the expire time for a file in an Azure Data Lake Store account.</span></span>

## <span data-ttu-id="d1b61-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d1b61-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b61-110">Exemplo 1: Definir o tempo de expiração de um arquivo</span><span class="sxs-lookup"><span data-stu-id="d1b61-110">Example 1: Set the expiration time for a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

<span data-ttu-id="d1b61-111">Define a expiração no arquivo myfile.txt na conta ContosoADL para daqui a duas horas.</span><span class="sxs-lookup"><span data-stu-id="d1b61-111">Sets expiration on the file myfile.txt in account ContosoADL to be two hours from now.</span></span>
<span data-ttu-id="d1b61-112">Isso fará com que o arquivo expire (ser marcado para exclusão) em duas horas.</span><span class="sxs-lookup"><span data-stu-id="d1b61-112">This will cause the file to expire (be marked for delete) in two hours.</span></span>

### <span data-ttu-id="d1b61-113">Exemplo 2: Remover a expiração em um arquivo</span><span class="sxs-lookup"><span data-stu-id="d1b61-113">Example 2: Remove the expiration on a file</span></span>
```
PS C:\> Set-AzDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

<span data-ttu-id="d1b61-114">Remove qualquer expiração definida anteriormente no arquivo "myfile.txt" na conta "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="d1b61-114">Removes any expiration that was previously set on file 'myfile.txt' in account 'ContosoADL'.</span></span>
<span data-ttu-id="d1b61-115">Isso significa que o arquivo não expirará automaticamente (será marcado para exclusão) e precisará ser excluído manualmente ou definido para expirar novamente.</span><span class="sxs-lookup"><span data-stu-id="d1b61-115">This means the file will not automatically expire (be marked for delete) and will need to be manually deleted or set to expire again.</span></span>

### <span data-ttu-id="d1b61-116">Exemplo 3: Definir o tempo de expiração de um arquivo em relação a agora</span><span class="sxs-lookup"><span data-stu-id="d1b61-116">Example 3: Set expiration time for a file relative to now</span></span>
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

<span data-ttu-id="d1b61-117">O primeiro comando define o tempo de expiração do arquivo /myfile.txt 240 segundos em relação à hora atual no servidor.</span><span class="sxs-lookup"><span data-stu-id="d1b61-117">The first command sets the expiration time of the file /myfile.txt 240 seconds relative to current time at server.</span></span>
<span data-ttu-id="d1b61-118">O segundo comando define o tempo de expiração do arquivo /myfile.txt 240 segundos em relação ao tempo de criação no servidor.</span><span class="sxs-lookup"><span data-stu-id="d1b61-118">The second command sets the expiration time of the file /myfile.txt 240 seconds relative to creation time at server.</span></span>

## <span data-ttu-id="d1b61-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1b61-119">PARAMETERS</span></span>

### <span data-ttu-id="d1b61-120">-Conta</span><span class="sxs-lookup"><span data-stu-id="d1b61-120">-Account</span></span>
<span data-ttu-id="d1b61-121">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1b61-121">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d1b61-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b61-122">-DefaultProfile</span></span>
<span data-ttu-id="d1b61-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d1b61-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1b61-124">-Expiração</span><span class="sxs-lookup"><span data-stu-id="d1b61-124">-Expiration</span></span>
<span data-ttu-id="d1b61-125">O tempo de expiração absoluto do arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d1b61-125">The absolute expiration time for the specified file.</span></span>
<span data-ttu-id="d1b61-126">Se nenhum valor ou definido como MaxValue, o arquivo nunca expirará.</span><span class="sxs-lookup"><span data-stu-id="d1b61-126">If no value or set to MaxValue, the file will never expire.</span></span>

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

### <span data-ttu-id="d1b61-127">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d1b61-127">-Path</span></span>
<span data-ttu-id="d1b61-128">Especifica o caminho do Data Lake Store do item de arquivo para o qual definir ou remover expirar.</span><span class="sxs-lookup"><span data-stu-id="d1b61-128">Specifies the Data Lake Store path of the file item for which to set or remove expiry.</span></span>

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

### <span data-ttu-id="d1b61-129">-RelativeFileExpiryOption</span><span class="sxs-lookup"><span data-stu-id="d1b61-129">-RelativeFileExpiryOption</span></span>
<span data-ttu-id="d1b61-130">Opções de expiração relativas.</span><span class="sxs-lookup"><span data-stu-id="d1b61-130">Relative expiry options.</span></span> <span data-ttu-id="d1b61-131">RelativeToData ou RelativeToCreationDate são opções atuais</span><span class="sxs-lookup"><span data-stu-id="d1b61-131">RelativeToNow or RelativeToCreationDate are current options</span></span>

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

### <span data-ttu-id="d1b61-132">-RelativeTime</span><span class="sxs-lookup"><span data-stu-id="d1b61-132">-RelativeTime</span></span>
<span data-ttu-id="d1b61-133">O tempo relativo em milissegundos em relação ao tempo de criação ou agora</span><span class="sxs-lookup"><span data-stu-id="d1b61-133">The relative time in milliseconds with respect to now or creation time</span></span>

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

### <span data-ttu-id="d1b61-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d1b61-134">-Confirm</span></span>
<span data-ttu-id="d1b61-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1b61-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1b61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1b61-136">-WhatIf</span></span>
<span data-ttu-id="d1b61-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d1b61-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1b61-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1b61-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1b61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b61-139">CommonParameters</span></span>
<span data-ttu-id="d1b61-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b61-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b61-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b61-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="d1b61-142">INPUTS</span></span>

### <span data-ttu-id="d1b61-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d1b61-143">System.String</span></span>

### <span data-ttu-id="d1b61-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d1b61-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d1b61-145">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d1b61-145">System.DateTimeOffset</span></span>

### <span data-ttu-id="d1b61-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span><span class="sxs-lookup"><span data-stu-id="d1b61-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions</span></span>

### <span data-ttu-id="d1b61-147">System.Int64</span><span class="sxs-lookup"><span data-stu-id="d1b61-147">System.Int64</span></span>

## <span data-ttu-id="d1b61-148">Saídas</span><span class="sxs-lookup"><span data-stu-id="d1b61-148">OUTPUTS</span></span>

### <span data-ttu-id="d1b61-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d1b61-149">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d1b61-150">Notas</span><span class="sxs-lookup"><span data-stu-id="d1b61-150">NOTES</span></span>
<span data-ttu-id="d1b61-151">Alias: Set-AdlStoreItemExpiry</span><span class="sxs-lookup"><span data-stu-id="d1b61-151">Alias: Set-AdlStoreItemExpiry</span></span>

## <span data-ttu-id="d1b61-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1b61-152">RELATED LINKS</span></span>

[<span data-ttu-id="d1b61-153">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d1b61-153">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

