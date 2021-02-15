---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115373"
---
# <span data-ttu-id="74fbb-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="74fbb-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="74fbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="74fbb-103">Modifica o proprietário de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74fbb-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="74fbb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74fbb-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74fbb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="74fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="74fbb-106">O cmdlet **Set-AzDataLakeStoreItemOwner** modifica o proprietário de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74fbb-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="74fbb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="74fbb-108">Exemplo 1: Definir o proprietário de um item</span><span class="sxs-lookup"><span data-stu-id="74fbb-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="74fbb-109">Esse comando define o proprietário para o diretório raiz como Sendo Ele.</span><span class="sxs-lookup"><span data-stu-id="74fbb-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="74fbb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74fbb-110">PARAMETERS</span></span>

### <span data-ttu-id="74fbb-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="74fbb-111">-Account</span></span>
<span data-ttu-id="74fbb-112">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="74fbb-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="74fbb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74fbb-113">-DefaultProfile</span></span>
<span data-ttu-id="74fbb-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="74fbb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74fbb-115">-ID</span><span class="sxs-lookup"><span data-stu-id="74fbb-115">-Id</span></span>
<span data-ttu-id="74fbb-116">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do AzureActive Directory a ser usado como proprietário.</span><span class="sxs-lookup"><span data-stu-id="74fbb-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="74fbb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74fbb-117">-PassThru</span></span>
<span data-ttu-id="74fbb-118">Indica que o proprietário atualizado resultante deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="74fbb-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="74fbb-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="74fbb-119">-Path</span></span>
<span data-ttu-id="74fbb-120">Especifica o caminho do Data Lake Store do item a ser modificado, começando pelo diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="74fbb-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="74fbb-121">-Tipo</span><span class="sxs-lookup"><span data-stu-id="74fbb-121">-Type</span></span>
<span data-ttu-id="74fbb-122">Especifica o tipo de proprietário a ser definido.</span><span class="sxs-lookup"><span data-stu-id="74fbb-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="74fbb-123">Os valores aceitáveis para este parâmetro são: Usuário e Grupo.</span><span class="sxs-lookup"><span data-stu-id="74fbb-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="74fbb-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74fbb-124">-Confirm</span></span>
<span data-ttu-id="74fbb-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74fbb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74fbb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74fbb-126">-WhatIf</span></span>
<span data-ttu-id="74fbb-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74fbb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74fbb-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74fbb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74fbb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74fbb-129">CommonParameters</span></span>
<span data-ttu-id="74fbb-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74fbb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74fbb-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74fbb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74fbb-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="74fbb-132">INPUTS</span></span>

### <span data-ttu-id="74fbb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="74fbb-133">System.String</span></span>

### <span data-ttu-id="74fbb-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="74fbb-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="74fbb-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="74fbb-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="74fbb-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="74fbb-136">System.Guid</span></span>

### <span data-ttu-id="74fbb-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74fbb-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74fbb-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="74fbb-138">OUTPUTS</span></span>

### <span data-ttu-id="74fbb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="74fbb-139">System.String</span></span>

## <span data-ttu-id="74fbb-140">Notas</span><span class="sxs-lookup"><span data-stu-id="74fbb-140">NOTES</span></span>

## <span data-ttu-id="74fbb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74fbb-141">RELATED LINKS</span></span>

[<span data-ttu-id="74fbb-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="74fbb-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


