---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 5f59796a51ccd1f3e5e77442cde434ab803d0781
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772131"
---
# <span data-ttu-id="14cad-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="14cad-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="14cad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14cad-102">SYNOPSIS</span></span>
<span data-ttu-id="14cad-103">Exclui uma conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="14cad-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="14cad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14cad-104">SYNTAX</span></span>

### <span data-ttu-id="14cad-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="14cad-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14cad-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14cad-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14cad-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14cad-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14cad-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14cad-108">DESCRIPTION</span></span>
<span data-ttu-id="14cad-109">O cmdlet **Remove-AzNetAppFilesAccount** exclui uma conta ANF.</span><span class="sxs-lookup"><span data-stu-id="14cad-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="14cad-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14cad-110">EXAMPLES</span></span>

### <span data-ttu-id="14cad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14cad-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="14cad-112">Esse comando exclui a conta ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="14cad-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="14cad-113">OS</span><span class="sxs-lookup"><span data-stu-id="14cad-113">PARAMETERS</span></span>

### <span data-ttu-id="14cad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cad-114">-DefaultProfile</span></span>
<span data-ttu-id="14cad-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14cad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14cad-116">-InputObject</span></span>
<span data-ttu-id="14cad-117">O objeto de conta a ser removido</span><span class="sxs-lookup"><span data-stu-id="14cad-117">The account object to remove</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14cad-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="14cad-118">-Name</span></span>
<span data-ttu-id="14cad-119">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="14cad-119">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14cad-120">-PassThru</span></span>
<span data-ttu-id="14cad-121">Retornar se a conta especificada foi removida com êxito</span><span class="sxs-lookup"><span data-stu-id="14cad-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="14cad-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14cad-122">-ResourceGroupName</span></span>
<span data-ttu-id="14cad-123">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="14cad-123">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14cad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14cad-124">-ResourceId</span></span>
<span data-ttu-id="14cad-125">A ID do recurso da conta ANF</span><span class="sxs-lookup"><span data-stu-id="14cad-125">The resource id of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14cad-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14cad-126">-Confirm</span></span>
<span data-ttu-id="14cad-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14cad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14cad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14cad-128">-WhatIf</span></span>
<span data-ttu-id="14cad-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14cad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14cad-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14cad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14cad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cad-131">CommonParameters</span></span>
<span data-ttu-id="14cad-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14cad-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14cad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cad-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14cad-134">INPUTS</span></span>

### <span data-ttu-id="14cad-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14cad-135">System.String</span></span>

### <span data-ttu-id="14cad-136">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="14cad-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="14cad-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14cad-137">OUTPUTS</span></span>

### <span data-ttu-id="14cad-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14cad-138">System.Boolean</span></span>

## <span data-ttu-id="14cad-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14cad-139">NOTES</span></span>

## <span data-ttu-id="14cad-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14cad-140">RELATED LINKS</span></span>
