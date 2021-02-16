---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 6c082d2e61f81c4e0b8cf9bebefd623584fac3e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113540"
---
# <span data-ttu-id="ccf25-101">Get-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ccf25-101">Get-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="ccf25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccf25-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf25-103">Obtém detalhes de uma configuração do Azure NetApp Files (ANF) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ccf25-103">Gets details of an Azure NetApp Files (ANF) Active Directory configuration.</span></span>

## <span data-ttu-id="ccf25-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccf25-104">SYNTAX</span></span>

### <span data-ttu-id="ccf25-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ccf25-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 [-ActiveDirectoryId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccf25-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccf25-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesActiveDirectory [-ActiveDirectoryId <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccf25-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ccf25-107">DESCRIPTION</span></span>
<span data-ttu-id="ccf25-108">O cmdlet **Get-AzNetAppFilesActiveDirectory** obtém detalhes de uma configuração do Active Directory de contas ANF.</span><span class="sxs-lookup"><span data-stu-id="ccf25-108">The **Get-AzNetAppFilesActiveDirectory** cmdlet gets details of an ANF accounts Active Directory configuration.</span></span>

## <span data-ttu-id="ccf25-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ccf25-109">EXAMPLES</span></span>

### <span data-ttu-id="ccf25-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ccf25-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyADConfigName"
```

<span data-ttu-id="ccf25-111">Esse comando obtém a configuração do AD chamada MyADConfigName para a conta AZure NetApp Files (ANF) chamada MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="ccf25-111">This command gets the AD configuration named MyADConfigName for the Azure NetApp Files (ANF) account named MyAnfAccount.</span></span>

## <span data-ttu-id="ccf25-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccf25-112">PARAMETERS</span></span>

### <span data-ttu-id="ccf25-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="ccf25-113">-AccountName</span></span>
<span data-ttu-id="ccf25-114">O nome da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ccf25-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf25-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="ccf25-115">-AccountObject</span></span>
<span data-ttu-id="ccf25-116">A Conta do novo objeto do Active Directory</span><span class="sxs-lookup"><span data-stu-id="ccf25-116">The Account for the new Active Directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf25-117">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="ccf25-117">-ActiveDirectoryId</span></span>
<span data-ttu-id="ccf25-118">O ActiveDirectoryId do ANF Active Directory</span><span class="sxs-lookup"><span data-stu-id="ccf25-118">The ActiveDirectoryId of the ANF Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActiveDirectoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf25-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf25-119">-DefaultProfile</span></span>
<span data-ttu-id="ccf25-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccf25-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccf25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf25-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccf25-122">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="ccf25-122">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf25-123">CommonParameters</span></span>
<span data-ttu-id="ccf25-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccf25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf25-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccf25-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf25-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="ccf25-126">INPUTS</span></span>

### <span data-ttu-id="ccf25-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="ccf25-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="ccf25-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="ccf25-128">OUTPUTS</span></span>

### <span data-ttu-id="ccf25-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="ccf25-129">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="ccf25-130">Notas</span><span class="sxs-lookup"><span data-stu-id="ccf25-130">NOTES</span></span>

## <span data-ttu-id="ccf25-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccf25-131">RELATED LINKS</span></span>
