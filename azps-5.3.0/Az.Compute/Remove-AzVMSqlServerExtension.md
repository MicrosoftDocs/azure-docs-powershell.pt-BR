---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 599b4817ce9f4f6f1f7a75f5811c5a3122f1bbb7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434238"
---
# <span data-ttu-id="ddb21-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ddb21-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="ddb21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddb21-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb21-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddb21-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="ddb21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddb21-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddb21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddb21-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb21-106">O cmdlet **Remove-AzVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddb21-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="ddb21-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddb21-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb21-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="ddb21-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="ddb21-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="ddb21-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="ddb21-110">OS</span><span class="sxs-lookup"><span data-stu-id="ddb21-110">PARAMETERS</span></span>

### <span data-ttu-id="ddb21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb21-111">-DefaultProfile</span></span>
<span data-ttu-id="ddb21-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddb21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb21-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddb21-113">-Name</span></span>
<span data-ttu-id="ddb21-114">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ddb21-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb21-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="ddb21-115">-NoWait</span></span>
<span data-ttu-id="ddb21-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ddb21-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ddb21-117">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="ddb21-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ddb21-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb21-118">-ResourceGroupName</span></span>
<span data-ttu-id="ddb21-119">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ddb21-119">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb21-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="ddb21-120">-VMName</span></span>
<span data-ttu-id="ddb21-121">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ddb21-121">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb21-122">CommonParameters</span></span>
<span data-ttu-id="ddb21-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb21-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddb21-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb21-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddb21-125">INPUTS</span></span>

### <span data-ttu-id="ddb21-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb21-126">System.String</span></span>

## <span data-ttu-id="ddb21-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddb21-127">OUTPUTS</span></span>

### <span data-ttu-id="ddb21-128">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ddb21-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ddb21-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddb21-129">NOTES</span></span>

## <span data-ttu-id="ddb21-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddb21-130">RELATED LINKS</span></span>

[<span data-ttu-id="ddb21-131">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ddb21-131">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="ddb21-132">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ddb21-132">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


