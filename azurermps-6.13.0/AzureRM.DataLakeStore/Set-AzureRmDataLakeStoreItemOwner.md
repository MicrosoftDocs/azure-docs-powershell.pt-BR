---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 0fd40207f72f83c68418d0184922301e137ffc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429577"
---
# <span data-ttu-id="97adf-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="97adf-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="97adf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97adf-102">SYNOPSIS</span></span>
<span data-ttu-id="97adf-103">Modifica o proprietário de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="97adf-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97adf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97adf-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97adf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97adf-105">DESCRIPTION</span></span>
<span data-ttu-id="97adf-106">O cmdlet **set-AzureRmDataLakeStoreItemOwner** modifica o proprietário de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="97adf-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="97adf-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97adf-107">EXAMPLES</span></span>

### <span data-ttu-id="97adf-108">Exemplo 1: definir o proprietário de um item</span><span class="sxs-lookup"><span data-stu-id="97adf-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="97adf-109">Esse comando define o proprietário do diretório raiz como Patti a Pereira.</span><span class="sxs-lookup"><span data-stu-id="97adf-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="97adf-110">OS</span><span class="sxs-lookup"><span data-stu-id="97adf-110">PARAMETERS</span></span>

### <span data-ttu-id="97adf-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="97adf-111">-Account</span></span>
<span data-ttu-id="97adf-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="97adf-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="97adf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97adf-113">-DefaultProfile</span></span>
<span data-ttu-id="97adf-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97adf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97adf-115">-ID</span><span class="sxs-lookup"><span data-stu-id="97adf-115">-Id</span></span>
<span data-ttu-id="97adf-116">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive a ser usado como proprietário.</span><span class="sxs-lookup"><span data-stu-id="97adf-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97adf-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97adf-117">-PassThru</span></span>
<span data-ttu-id="97adf-118">Indica que o proprietário atualizado resultante deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="97adf-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="97adf-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="97adf-119">-Path</span></span>
<span data-ttu-id="97adf-120">Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="97adf-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="97adf-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="97adf-121">-Type</span></span>
<span data-ttu-id="97adf-122">Especifica o tipo de proprietário a ser definido.</span><span class="sxs-lookup"><span data-stu-id="97adf-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="97adf-123">Os valores aceitáveis para esse parâmetro são: usuário e grupo.</span><span class="sxs-lookup"><span data-stu-id="97adf-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97adf-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97adf-124">-Confirm</span></span>
<span data-ttu-id="97adf-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97adf-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97adf-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97adf-126">-WhatIf</span></span>
<span data-ttu-id="97adf-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97adf-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97adf-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97adf-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97adf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97adf-129">CommonParameters</span></span>
<span data-ttu-id="97adf-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97adf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97adf-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97adf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97adf-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97adf-132">INPUTS</span></span>

### <span data-ttu-id="97adf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="97adf-133">System.String</span></span>

### <span data-ttu-id="97adf-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="97adf-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="97adf-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="97adf-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="97adf-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="97adf-136">System.Guid</span></span>

### <span data-ttu-id="97adf-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97adf-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97adf-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97adf-138">OUTPUTS</span></span>

### <span data-ttu-id="97adf-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97adf-139">System.Boolean</span></span>

## <span data-ttu-id="97adf-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97adf-140">NOTES</span></span>

## <span data-ttu-id="97adf-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97adf-141">RELATED LINKS</span></span>

[<span data-ttu-id="97adf-142">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="97adf-142">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


