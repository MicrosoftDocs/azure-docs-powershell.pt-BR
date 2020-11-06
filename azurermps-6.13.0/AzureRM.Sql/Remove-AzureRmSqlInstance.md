---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433180"
---
# <span data-ttu-id="b144f-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="b144f-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="b144f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b144f-102">SYNOPSIS</span></span>
<span data-ttu-id="b144f-103">Remove uma instância de banco de dados gerenciado do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b144f-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b144f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b144f-104">SYNTAX</span></span>

### <span data-ttu-id="b144f-105">RemoveInstanceFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="b144f-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b144f-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="b144f-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b144f-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="b144f-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b144f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b144f-108">DESCRIPTION</span></span>
<span data-ttu-id="b144f-109">O cmdlet **Remove-AzureRmSqlInstance** remove uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b144f-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="b144f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b144f-110">EXAMPLES</span></span>

### <span data-ttu-id="b144f-111">Exemplo 1: remover instância</span><span class="sxs-lookup"><span data-stu-id="b144f-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b144f-112">Esse comando Remove a instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="b144f-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="b144f-113">OS</span><span class="sxs-lookup"><span data-stu-id="b144f-113">PARAMETERS</span></span>

### <span data-ttu-id="b144f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b144f-114">-DefaultProfile</span></span>
<span data-ttu-id="b144f-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b144f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b144f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b144f-116">-Force</span></span>
<span data-ttu-id="b144f-117">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="b144f-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b144f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b144f-118">-InputObject</span></span>
<span data-ttu-id="b144f-119">O objeto AzureSqlManagedInstanceModel para remover</span><span class="sxs-lookup"><span data-stu-id="b144f-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b144f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b144f-120">-Name</span></span>
<span data-ttu-id="b144f-121">Nome da instância SQL.</span><span class="sxs-lookup"><span data-stu-id="b144f-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b144f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b144f-122">-ResourceGroupName</span></span>
<span data-ttu-id="b144f-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b144f-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b144f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b144f-124">-ResourceId</span></span>
<span data-ttu-id="b144f-125">A ID do recurso do objeto de instância a ser removido</span><span class="sxs-lookup"><span data-stu-id="b144f-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b144f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b144f-126">-Confirm</span></span>
<span data-ttu-id="b144f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b144f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b144f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b144f-128">-WhatIf</span></span>
<span data-ttu-id="b144f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b144f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b144f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b144f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b144f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b144f-131">CommonParameters</span></span>
<span data-ttu-id="b144f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b144f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b144f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b144f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b144f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b144f-134">INPUTS</span></span>

### <span data-ttu-id="b144f-135">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b144f-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="b144f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b144f-136">System.String</span></span>

## <span data-ttu-id="b144f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b144f-137">OUTPUTS</span></span>

### <span data-ttu-id="b144f-138">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="b144f-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="b144f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b144f-139">NOTES</span></span>

## <span data-ttu-id="b144f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b144f-140">RELATED LINKS</span></span>
